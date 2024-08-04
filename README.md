# Documentação

Para criar as User Story usei como referência sites reais que possuem as funcionalidades apresentadas no teste, e das referências que peguei, selecionei as regras de negócio que faziam sentido no contexto do teste, considerei também que a User Story que eu iria escrever seria aplicada a um produto real, portanto foquei em cria-la pensando no seu resultado final e não me baseando em como a funcionalidade está atualmente no teste.

# Cadastro de Curso - User Story

**Como um** usuário interno, **eu quero** cadastrar cursos, **para que** alunos possam se inscrever nos cursos.

## Critérios de Aceitação

1. **A seção deve conter os seguintes campos**:
    - Nome do Curso
        - Deve ser obrigatório
        - Deve ter um limite de 100 caracteres
    - Descrição do Curso
        - Deve ser obrigatório
        - Deve permitir a digitação de letras, números, caracteres especiais
        - Não deve permitir caracteres inválidos, como emojis ou símbolos
        - Deve conter algum simbolo no canto inferior direito indicando que a caixa de texto pode ser reduzida ou aumentada
    - Instrutor
        - Deve ser obrigatório
        - Deve aceitar apenas letras
        - Deve ter um limite de 100 caracteres
    - Url da Imagem de Capa
        - Deve ser obrigatório
        - Deve permitir a digitação de letras, números, caracteres especiais
    - Data de Início
        - Deve ser obrigatório
        - Deve permitir apenas números
        - Não deve permitir data de início anterior a data atual
        - Deve ser preenchido no formato mm/dd/yyyy
        - Deve conter um icone de calendário no canto direito para que a data possa ser selecionada visualmente
    - Data de Fim
        - Deve ser obrigatório
        - Deve permitir apenas números
        - Não deve permitir data de fim anterior a data de início
        - Deve ser preenchido no formato mm/dd/yyyy
        - Deve conter um icone de calendário no canto direito para que a data possa ser selecionada visualmente
    - Número de Vagas
        - Deve ser obrigatório
        - Deve permitir apenas números
        - Deve conter icones de seta para cima e para baixo para que os numeros possam ser acrescentados ou reduzidos ao clicar
    - Tipo de Curso
        - Deve ser obrigatório
        - Não deve aceitar nenhuma digitação
        - Ao clicar no campo deve aparecer 3 opções, 'Selecione...', 'Presencial' e 'Online'
            - Ao clicar na opção 'Selecione...' deve minimizar as opções
            - Ao clicar na opção 'Presencial' deve sugir a caixa de texto de Endereço
                - Deve ser obrigatório
                - Não deve permitir caracteres especiais
                - Deve ter um limite de 100 caracteres
            - Ao clicar na opção 'Online' deve surgir a caixa de texto do Link de Inscrição
                - Deve ser obrigatório
                - Deve aceitar todos os caracteres
    - Botão Cadastrar Curso
        - Ao clicar no botão deve mostrar um pop up 'Curso Cadastrado com Sucesso' no topo da tela
        - Ao cadastrar curso deve redirecionar o usuario para a pagina de 'listar cursos'
# Listar Curso - User Story

**Como um** usuário, **eu quero** listar cursos, **para que** eu possa visualizar facilmente todos os cursos disponíveis.

## Critérios de Aceitação

1. **A seção deve conter os seguintes campos**:
    - Deve ser exibido em formado de tabelas
    - Deve ser exibido por ordem alfabética
    - Deve conter um botão de 'Deletar Curso' embaixo de cada um dos cursos
    - A lista deve exibir uma pré visualização das informações dos cursos
        - Deve mostrar a imagem selecionada na criação do curso
        - Deve exibir se é presencial ou online
        - Deve exibir a descrição do curso
        - Deve exibir a data de inicio e de fim do curso
        - Deve exibir a quantidade de vagas disponíveis

# Deletar Curso - User Story

**Como um** usuário interno, **eu quero** deletar cursos, **para que** eu possa deletar cursos previamente criados.

## Critérios de Aceitação

1. **A seção deve conter os seguintes campos**:
    - Funcionalidade deve ser apenas exibida para funcionários internos.
    - Ao clicar no campo 'Deletar Curso' deve mostrar um pop up de confirmação para deletar.
    - Quando o curso for deletado deve aparecer um pop up no topo da tela com o texto 'Curso Excluído com Sucesso'
    - Quando o curso for deletado ele não deve aparecer mais na aba 'Listar Cursos'