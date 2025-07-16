---
title: Instruções para o exercício
permalink: index.html
layout: home
---

# Exercícios

Esta página relaciona os exercícios associados ao curso de habilidades da Microsoft **MS-4022: estender o Microsoft 365 Copilot no Copilot Studio**.

Roteiro de aprendizagem relacionado: [Estender o Microsoft 365 Copilot no Copilot Studio](https://learn.microsoft.com/training/paths/extend-microsoft-365-copilot-studio/).

**Observação**: para concluir esses exercícios, você precisará de:

- Uma conta corporativa ou de estudante com [acesso ao Copilot Studio](https://learn.microsoft.com/microsoft-copilot-studio/requirements-licensing-subscriptions). Se você ainda não tiver acesso ao Copilot Studio, dependendo da configuração da sua organização do Microsoft 365, poderá [criar uma conta de avaliação](https://learn.microsoft.com/microsoft-copilot-studio/sign-up-individual).
- Uma licença do Microsoft 365 Copilot
- Credenciais para se conectar às fontes de conteúdo desejadas (conectores, APIs etc.)

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %} {% assign labs = labs | sort: "lab.title" %} {% for activity in labs  %}
- [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) {% endfor %}

