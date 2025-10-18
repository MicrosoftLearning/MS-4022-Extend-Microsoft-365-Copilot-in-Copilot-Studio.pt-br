---
lab:
  title: 2.1 Criar uma ação de prompt
---

# Criar uma ação de prompt

Neste exercício, você criará uma ação de prompt, testará o prompt no Copilot Studio e testará o prompt em um agente do Copilot. Você criará uma ação de prompt que ajuda os usuários a transformar suas ideias brutas em argumentos de marketing organizados que seguem um formato e diretrizes específicos.

Este exercício deve levar aproximadamente **15** minutos para ser concluído.

## Criar um prompt personalizado no Copilot Studio

1. Abra o Copilot Studio em seu navegador da Web navegando até o [Copilot Studio](https://copilotstudio.microsoft.com) em `https://copilotstudio.microsoft.com`.
1. Selecione **Ferramentas** na navegação à esquerda.
1. Selecione **Nova ferramenta**.
1. Na janela pop-up Nova ferramenta, selecione **Solicitar**. Você vai acessar a interface do usuário do construtor de prompts.
1. Na caixa de texto **Instruções**, insira `Create a marketing pitch for a product based on a `.
1. Coloque o cursor no final da frase que você inseriu e selecione **Adicionar conteúdo**
1. Selecione **Texto**.
1. No campo **Nome**, insira `draft`.
1.  No campo **Dados de amostra**, insira `The Mighty Mechanical Pencil is new, exciting, and useful. It's not only the first of its kind pencil, but it's fun to use.` e selecione **Fechar**.

    ![Captura de tela da interface do usuário do construtor de prompts no Copilot Studio mostrando uma variável de entrada sendo configurada com o nome "rascunho".](../Media/prompt-action-input.png)

## Testar e refinar seu prompt

1. Selecione **Testar** acima da caixa de instruções para testar o prompt com os dados de exemplo fornecidos.
1. Visualizar o resultado da execução de testes.

Vamos refinar o prompt para criar uma saída mais estruturada e consistente.

1. Na caixa de texto **Instruções**, adicione o seguinte às instruções existentes para modificar o prompt:

    ```The pitch should follow the following Contoso guidelines:
       - Start with a brief hook
       - Describe unique value proposition
       - End with a call-to-action
       - Use an exciting and influential tone
    ```

1. Selecione **Testar** novamente para testar novamente o prompt.
1. Observe como a resposta difere.
1. Selecione **Salvar**.

## Configurar e publicar seu prompt

Depois de salvar o prompt, a janela **Configurar para usar no Agente** será exibida.

1. No campo **nome**, insira `Create a Contoso Marketing Pitch`.
1. No campo **Descrição para o agente saber quando usar essa ferramenta**, insira e `Create a marketing pitch that follows Contoso guidelines` selecione **Avançar**. Você será redirecionado à página **Criar prompt**.
1. Selecione **Adicionar**.

## (Opcional) Adicionar uma ação de prompt a um agente

Se você concluiu o laboratório anterior e criou um agente declarativo, pode adicionar essa ação ao seu agente e atualizar as instruções do agente para fazer referência à ação.

### Adicionar a ferramenta de prompt

1. Na barra lateral no Copilot Studio, selecione **Agentes**.
1. Selecione **Microsoft 365 Copilot**.
1. Em **Agentes**, selecione o agente de **Suporte ao Produto** ao qual você deseja adicionar a ação.
1. Na seção **Ferramentas** da página, selecione **Adicionar ferramenta**.
1. Selecione o filtro **Prompt**.
1. Selecione o prompt **Criar uma Apresentação de Marketing da Contoso**.
1. Selecione **Adicionar ao agente**. A ferramenta agora está listada nas **Ferramentas** do agente de Suporte ao Produto.

### Atualizar as instruções do agente

Atualize as instruções do agente para fornecer diretrizes para usar o prompt.

1. Na caixa de texto **Instruções** , adicione o seguinte ao texto de instruções existente: `Use the Contoso Marketing Pitch action to help marketing stakeholders craft pitches for products based on their draft ideas.`

Você concluiu o exercício e criou uma ferramenta de prompt para seu agente.
