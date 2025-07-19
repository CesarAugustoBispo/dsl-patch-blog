---
title: "Contribuição ao Kernel – IIO Driver"
date: 2025-07-18
layout: post
tags: [linux, kernel, flatseal, debian, contribuições, open-source]

---
## Contribuições Recentes – DSL 2025

### Contribuições ao Driver IIO (`qcom-pm8xxx-xoadc`)

**Objetivo:** Substituir o uso de `devm_regulator_get()` por `devm_regulator_get_enable()` para garantir melhor gerenciamento de recursos, evitando vazamentos e simplificando a lógica do driver.

#### Histórico dos Patches Enviados:

1. **Primeira submissão**  
   Substituição direta de funções por suas variantes `devm_..._enable`.  
   **Status:** Recebemos sugestões de melhoria (estilo e reuso de código).

   ![Diagrama do patch IIO](/dsl-patch-blog/assets/unnamed.png)
   ![Diagrama do patch IIO](/dsl-patch-blog/assets/unnamed(1).png)

3. **Segunda submissão**  
   Refatoração parcial com melhorias de estilo e legibilidade.  
   **Status:** Novo envio limpando a abordagem original.

   ![Diagrama do patch IIO](/dsl-patch-blog/assets/unnamed(2).png)

5. **Patch final:**  
   Refatoração completa do `probe()` e limpeza do `remove()`  
   **Status:**  
   ✅ *Patch aplicado por Jonathan Cameron*, com o seguinte comentário:
   > "Fiz uma última mudança ao aplicar: incluí o nome do driver no título do patch. Está em branch de testes, será rebaseado no rc1."

   📌 *Próximo passo sugerido:* usar `devm_iio_device_register()` e eliminar o `remove()` por completo.

   ![Diagrama do patch IIO](/dsl-patch-blog/assets/unnamed(3).png)
---

### Experiência e reflexões

Essa contribuição marcou o início de uma participação mais ativa no kernel Linux. Aprendi bastante sobre as funções `devm_` e o gerenciamento automático de recursos, algo que não era tão evidente para mim antes.

O processo de revisão foi exigente, especialmente para manter o padrão de legibilidade e reutilização de variáveis. A interação com o mantenedor Jonathan Cameron me deu segurança para seguir contribuindo — e me mostrou como um feedback técnico bem feito pode orientar nosso crescimento. Senti orgulho quando o patch foi aplicado!
