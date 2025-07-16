---
lab:
  title: 2.1 Criar uma ação de prompt
---

# Criar uma ação de prompt

Neste exercício, você criará uma ação de prompt, testará o prompt no Copilot Studio e testará o prompt em um agente do Copilot. Você criará uma ação de prompt que ajuda os usuários a transformar suas ideias brutas em argumentos de marketing organizados que seguem um formato e diretrizes específicos.

Este exercício deve levar aproximadamente **15** minutos para ser concluído.

## Criar uma ação de prompt no Copilot Studio

1. Abra o Copilot Studio em seu navegador da Web navegando até o [Copilot Studio](https://copilotstudio.microsoft.com) em `https://copilotstudio.microsoft.com`.
1. Selecione **Biblioteca** no painel de navegação à esquerda.
1. Selecione **Adicionar novo** e, em seguida, selecione **Prompt**. O assistente **Adicionar uma ação de prompt** é aberto.
1. No campo **Nome**, insira `Create a Contoso Marketing Pitch`.
1. No campo **Descrição**, digite `Create a marketing pitch that follows Contoso guidelines` em seguida, selecione **Avançar**. Você será redirecionado à página **Criar prompt**.
1. Na caixa de texto **Instruções**, insira `Create a marketing pitch for a product based on a `.
1. Coloque o cursor no final da frase que você inseriu e selecione **Adicionar conteúdo**
1. Selecione **Texto**.
1. No campo **Nome**, insira `draft`.
1. No campo **Dados de amostra**, insira `The Mighty Mechanical Pencil is new, exciting, and useful. It's not only the first of its kind pencil, but it's fun to use.` e selecione **Fechar**.

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

## Configurar e publicar sua ação

1. Na página **Selecionar parâmetros de ação**, forneça a seguinte **descrição** para a `draft` variável de entrada: `initial draft of the marketing pitch`.
1. Forneça a seguinte **descrição** da `text` variável de saída: `Final marketing pitch that adheres to Contoso guidelines`.
1. Selecione **Avançar**.
1. Verifique se você inseriu os detalhes corretamente e selecione **Publicar**.
1. Aguarde alguns instantes enquanto sua ação é salva e publicada.
1. Sua ação agora está disponível na Biblioteca. Selecione **Salvar e fechar**.

   > **Observação**: sua nova ação de prompt pode levar vários minutos ou mais para aparecer nas seções **Em destaque** ou **Biblioteca** da página **Adicionar ação** de um agente.

## (Opcional) Adicionar uma ação de prompt a um agente

Se você concluiu o laboratório anterior e criou um agente declarativo, pode adicionar essa ação ao seu agente e atualizar as instruções do agente para fazer referência à ação.

### Adicionar a ação.

1. Na **Biblioteca** , selecione o agente declarativo ao qual você deseja adicionar a ação.
1. Na seção **Detalhes**, selecione **Editar**.
1. Na caixa de texto **Instruções** , adicione o seguinte ao texto de instruções existente: `Use the Contoso Marketing Pitch action to help marketing stakeholders craft pitches for products based on their draft ideas.`
1. Na página de detalhes do agente, em **Ações**, selecione **Adicionar ação**.
1. Nas seções **Em Destaque** ou **Biblioteca** da janela modal **Adicionar ação** , selecione **Apresentação de Marketing da Contoso**.
1. Na página de ação, verifique se o **Nome** é `Create a Contoso Marketing Pitch`
1. Certifique-se de que a **descrição** seja `Create a marketing pitch that follows the Contoso guidelines`.
1. Selecione **Adicionar ação**. Isso pode demorar alguns instantes. A ação é adicionada à lista de ações disponíveis para o agente em **Ações**.

### Configurar a ação

1. Selecione a ação `Contoso Marketing Pitch` a partir das ações disponíveis para o agente. Você é encaminhado a uma página para definir as propriedades e configurações da ação.
1. Confirme se o **Nome da ação** está definido como `Create a new Contoso marketing pitch`.
1. Selecione **Entradas** na navegação superior dentro da ação.
1. Em **Entradas adicionais**, selecione **Adicionar**.
1. Selecione a variável **Rascunho**. Um formulário é exibido.
1. Certifique-se de que o campo **Como o agente preencherá esta entrada** esteja definido como **Preencher dinamicamente com a melhor opção (padrão).**
1. No campo **Nome de exibição**, insira `Initial draft`.
1. Verifique se o campo **Identificar como** está definido como **Resposta completa do usuário**
1. Selecione **Salvar** na parte superior direita da janela.

## (opcional) Testar ação de prompt no Copilot Studio.

Em seguida, teste o agente com a ação no Copilot Studio.

1. No painel **Testar seu agente** na página de visão geral do agente no Copilot Studio, selecione o botão **atualizar** para atualizar o painel de teste e carregar as alterações mais recentes do agente.
1. Na caixa de texto da conversa de teste, digite `Create a Contoso marketing pitch based on the following draft: "Bouncy ball is the hottest product on the market for both youth and adults. It's durable and the largest of its kind."` e envie a mensagem.
1. Revise a resposta e observe que o agente está seguindo as diretrizes fornecidas nas instruções da ação de prompt personalizado.

Você concluiu o exercício e validou a funcionalidade de sua ação imediata.
