---
title: Configuração de Ambiente com QEMU e libvirt
date: 2025-02-26
---

## Introdução

Este tutorial descreve como configurar um ambiente de testes para desenvolvimento do kernel Linux utilizando **QEMU** e **libvirt**, permitindo compilar e instalar kernels personalizados a partir do código-fonte de forma segura e eficiente.

Este é o primeiro de uma série de quatro tutoriais que introduzem iniciantes ao desenvolvimento do kernel Linux, utilizando o subsistema **Industrial I/O (IIO)** como espaço prático para aprendizagem prática.

## Experiência Pessoal

Foram realizados todos os passos desse tutorial sem dificuldades, **exceto na parte de configuração do SSL**, onde foi necessário consultar alguns materiais externos.

A configuração **opcional** _Set up host <-> VM file sharing_ acabou impactando os demais tutoriais de forma negativa, sendo necessário **reverter a configuração** para garantir a continuidade do processo nos tutoriais seguintes.

## Conclusão

A configuração do ambiente com QEMU e libvirt mostrou-se eficiente e segura para testes de desenvolvimento do kernel. Problemas pontuais com SSL e compartilhamento de arquivos entre host e VM podem surgir, mas são contornáveis com ajustes manuais e atenção à documentação complementar.
