---
layout: default
title: Meu Diário de Bordo
---

# 🚀 Diário de Bordo

Bem-vindo ao nosso espaço de compartilhamento de aprendizados e experiências.

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url }})
🗓️ {{ post.date | date: "%d/%m/%Y" }}

{{ post.excerpt }}
{% endfor %}
