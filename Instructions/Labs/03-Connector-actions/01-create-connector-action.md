---
lab:
  title: '3.1: Criar uma ação de conector'
---

# Criar uma ação de conector

Neste exercício, você configurará uma ação de conector para um agente declarativo no Copilot Studio. Você usará o conector "SharePoint – Pasta de lista" para recuperar uma lista de arquivos de uma pasta Produtos que contém arquivos de suporte ao produto.

Este exercício deve levar aproximadamente **15** minutos para ser concluído.

## Antes de começar

Este exercício se concentra na adição de ações do conector a um agente existente. Este exercício pressupõe o seguinte:

1. você já criou um agente declarativo de **suporte ao produto** no Copilot Studio. Se você precisar de instruções para criar um agente declarativo, consulte: [Criar um agente declarativo](../01-Build-your-first-declarative-agent/01-create-declarative-agent.md).
1. Você tem um site do SharePoint intitulado **Suporte ao Produto** que contém uma biblioteca de documentos chamada **Produtos** contendo arquivos com dados de exemplo relacionados ao produto. Para obter instruções, consulte a seção **Antes de começar** no exercício: [Adicionar conhecimento personalizado](../01-Build-your-first-declarative-agent/02-add-custom-knowledge.md).

## Criar uma ação do conector do SharePoint

1. No navegador da Web, navegue até o [Copilot Studio](https://www.copilotstudio.microsoft.com) em `https://www.copilotstudio.microsoft.com`.
1. Na **Biblioteca**selecione o agente de **Suporte ao Produto** .
1. Em **ações**, selecione **Adicionar ação**.
1. Na janela **Adicionar ação**, digite `SharePoint` na barra **Pesquisar**. Aguarde até que as ações relevantes sejam exibidas na janela.
1. Navegue e selecione a ação do conector **Pasta de lista do SharePoint**.
1. A janela modal exibe uma conexão para o conector do SharePoint. Uma marca de seleção verde será exibida ao lado do conector quando sua conexão estiver ativa. Você pode selecionar o **...** para exibir detalhes sobre a conexão.
    ![Captura de tela mostrando o status das conexões.](../Media/SharePoint-connection.png)
1. Selecione **Avançar** quando a conexão estiver ativa. Você será direcionado para a página **Pasta de lista** para configurar as propriedades da ação.
1. Na caixa de texto **Nome**, insira `List product support files`.
1. Insira `List product support files available in the Products folder` na caixa de texto descrição **Descrição**.
1. Confirme se a **Autenticação do usuário final** está definida como **Autenticação do usuário**.
1. Expanda a seção de **entradas e saídas**.
1. Selecione a entrada **Endereço do site**.
1. Na caixa de texto **Valor**, insira o URL do site do SharePoint de **Suporte ao Produto** no formato `https://DOMAIN.sharepoint.com/sites/ProductSupport` e selecione **Concluído**.
1. Selecione a entrada **Identificador de arquivo**.
1. Defina **Como o agente preencherá essa entrada?** para **Definir como um valor** da lista suspensa e selecione **Confirmar**.
1. Na caixa de texto **Valor**, insira `Products` e selecione **Concluído**.
1. Selecione o botão **Adicionar ação** e aguarde até que a ação do SharePoint seja adicionada ao seu agente. A ação agora deve ser listada na seção **Ações** da página de detalhes do agente.

## Configurar a ação

1. Na seção **Ações**, selecione a ação **Listar arquivos de suporte do produto** para abrir a página de detalhes.
1. Navegue até a guia **Saídas**.
1. Para fins de teste, em **Escolher como o resultado desta ação será exibido**, marque a caixa **Enviar uma mensagem imediatamente após executar a ação**. Uma opção de configuração adicional será exibida.
1. Selecione o menu suspenso em **Como você deseja exibir informações para o usuário?** e selecione **Você cria uma mensagem**. Uma caixa de texto será exibida.
1. Na caixa de texto **Mensagem a ser exibida** , digite `You used the SharePoint connector` e selecione **Salvar** na parte superior da página.

## Modificar as instruções do agente

Vamos também atualizar as instruções do seu agente que fornecem diretrizes para usar a ação do conector.

1. Na seção **Detalhes** do seu agente **Suporte ao Produto**, selecione **Editar**.
1. Na caixa de texto **Instruções**, adicione o seguinte ao texto de instruções existente: `When asked about available support resources, use the SharePoint connector to list the files in the Products folder.`
1. Selecione **Salvar**.

## Teste seu agente com a ação

1. Expanda o painel **Testar agente** no lado direito da página de detalhes do agente.
1. Selecione o botão de **atualização** no painel de teste para carregar as alterações mais recentes do agente.
1. Na caixa de mensagem, digite `What product support files are available?` e envie a mensagem.
1. Observe que o agente responde com a mensagem "Você usou o conector do SharePoint" e, em seguida, lista os arquivos disponíveis na pasta Produtos.

Você validou que a ação do conector funciona conforme o esperado no agente.
