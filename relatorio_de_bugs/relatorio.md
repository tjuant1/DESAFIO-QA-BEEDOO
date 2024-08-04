# Relatório de Bugs

### Documentação

Para estruturar meu relatório com os bugs encontrado vou utilizar uma metodologia baseada Norma IEEE 829 que apresenta uma estrutura detalhada e completa sendo o ideal na minha visão para documentar bugs, outro motivo para sustentar minha escolha é o fato de ser um padrão de documentação amplamente utilizado, o que significa que é comprovadamente eficaz e de facil entendimento para todas as áreas envolvidas.

# Bug 001: Erro 405 ao tentar deletar um curso

### Descrição:
Ao tentar deletar um curso, recebo a resposta 'Curso Excluído com Sucesso' porém o curso permanece visível na aba 'Listar Cursos' e o erro 405 é apresentado no console do navegador.


### Passos para Reproduzir
```
1. Esteja na pagina de 'Listar Cursos'.
2. Cique em 'Excluir Curso'.
3. Observe o erro retornado.
```
### Resultados esperados
```
O curso devería ser excluido e não aparecer mais na aba 'Listar Cursos'
```
### Prioridade e Severidade
```
 - Prioridade: Alta
 - Severidade: Alta
```

# Bug 002: Nenhum campo do cadastro de curso é obrigatório

### Descrição:
Na tela de 'Cadastrar Curso' é possível cadastrar um novo curso sem preencher nenhuma informação.

### Passos para Reproduzir
```
1. No site Beedoo QA Chalenge, clique em 'Cadatrar Curso'
2. Não preencha nenhum campo.
3. Clique em cadastrar curso.
4. Navegue até 'Listar Curso'
4. Observe o curso criado.
```
### Resultados esperados
```
A criação do curso deveria falhar e o usuário deveria receber uma mensagem dizendo que é necessário preencher os campos obrigatórios
```
### Prioridade e Severidade
```
 - Prioridade: Alta
 - Severidade: Alta
```

# Bug 003: Cadastrar cursos iguais

### Descrição:
Na tela de 'Cadastrar Curso' é possível cadastrar um novo curso preenchendo exatamente as mesmas informaçõe que um curso já existente.

### Passos para Reproduzir
```
1. No site Beedoo QA Chalenge, clique em 'Cadatrar Curso'
2. Preencha as mesmas informações que algum outro curso que já foi criado.
3. Clique em cadastrar curso.
4. Observe o erro retornado.
```
### Resultados esperados
```
A criação do curso deveria falhar e o usuário deveria receber uma mensagem dizendo que curso já existe no banco de dados
```
### Prioridade e Severidade
```
 - Prioridade: Média
 - Severidade: Média
```

# Bug 004: Cadastrar cursos com link inválido de imagem 

### Descrição:
Na tela de 'Cadastrar Curso' é possível cadastrar um novo curso com o campo 'URL da imagem de capa' contendo informações aleatórias.

### Passos para Reproduzir
```
1. No site Beedoo QA Chalenge, clique em 'Cadatrar Curso'
2. Coloque uma palavra aleatória no campo 'URL da imagem de capa'
3. Preencha os outros campos
3. Clique em cadastrar curso.
4. Observe o erro retornado.
```
### Resultados esperados
```
A criação do curso deveria falhar e o usuário deveria receber uma mensagem dizendo que esta url não é válida
```
### Prioridade e Severidade
```
 - Prioridade: Baixa
 - Severidade: Baixa
```

# Bug 005: CORB impedindo o carregamento das imagens de capa dos cursos

### Descrição:
Na tela de 'Listar Cursos' as imagens de capa dos cursos não são exibidas pois a configuração do CORB não está permitindo a exibição de links terceiros.

### Passos para Reproduzir
```
1. No site Beedoo QA Chalenge, clique em 'Listar Cursos'
2. Observe o erro retornado.
```
### Resultados esperados
```
Todas as imagens de capa dos cursos deveriam ser exibidas.
```
### Prioridade e Severidade
```
 - Prioridade: Baixa
 - Severidade: Baixa
```

# Bug 006: Cadastrar curso online sem o link da insrição

### Descrição:
Na tela de 'Cadastrar Cursos' é possível concluir o cadastro de um curso sem adicionar o link de inscrição de um curso online.

### Passos para Reproduzir
```
1. No site Beedoo QA Chalenge, clique em 'Cadastrar Cursos
2. Selecione o tipo de curso como 'Online'
3. Preencha os outros campos
4. Deixe o campo 'Link de Inscrição' em branco
5. Clique em Cadastrar Curso
6. Observe o erro retornado.
```
### Resultados esperados
```
A criação do curso deveria falhar e o usuário deveria receber uma mensagem dizendo que o link de inscrição é obrigatório
```
### Prioridade e Severidade
```
 - Prioridade: Média
 - Severidade: Média
```

# Bug 007: Cadastrar curso com a data de fim anterior a data de início

### Descrição:
Na tela de 'Cadastrar Cursos' é possível concluir o cadastro de um curso mesmo que a data do fim do curso seja anterior a data de inicio.

### Passos para Reproduzir
```
1. No site Beedoo QA Chalenge, clique em 'Cadastrar Cursos
2. Coloque a 'Data de Início' como hoje 
3. Preencha os outros campos
4. Coloque a 'Data de Fim' como ontem
5. Clique em Cadastrar Curso
6. Observe o erro retornado.
```
### Resultados esperados
```
A criação do curso deveria falhar e o usuário deveria receber uma mensagem dizendo que a data de fim do curso não pode ser anterior a data de início
```
### Prioridade e Severidade
```
 - Prioridade: Baixa
 - Severidade: Baixa
```

# Bug 008: Cadastrar curso com vagas negativas

### Descrição:
Na tela de 'Cadastrar Cursos' é possível concluir o cadastro de um curso com o número de vagas negativas.

### Passos para Reproduzir
```
1. No site Beedoo QA Chalenge, clique em 'Cadastrar Cursos
2. Coloque o 'Número de Vagas' como um valor negativo aleatório
3. Preencha os outros campos
4. Clique em Cadastrar Curso
5. Observe o erro retornado.
```
### Resultados esperados
```
A criação do curso deveria falhar e o usuário deveria receber uma mensagem dizendo que o número de vagas não pode ser negativo.
```
### Prioridade e Severidade
```
 - Prioridade: Baixa
 - Severidade: Baixa
```

# Bug 009: Cadastrar curso com infinitos caracteres

### Descrição:
Na tela de 'Cadastrar Cursos' é possível concluir o cadastro de um curso após colocar centenas de caracteres no Nome do curso.
### Passos para Reproduzir
```
1. No site Beedoo QA Chalenge, clique em 'Cadastrar Cursos
2. Coloque uma quantidade gigante de caracteres no Nome do Curso
3. Preencha os outros campos
4. Clique em Cadastrar Curso
5. Navegue até 'Listar Curso'
5. Observe que na listagem de cursos a tabela perde a formatação pro conta da quantidade de caracteres.
```
### Resultados esperados
```
A criação do curso deveria falhar e o usuário deveria receber uma mensagem dizendo que o limite de caracteres é 100.
```
### Prioridade e Severidade
```
 - Prioridade: Baixa
 - Severidade: Baixa
```
# Bug 010: Cadastrar curso presencial sem endereço

### Descrição:
Na tela de 'Cadastrar Cursos' é possível concluir o cadastro de um curso sem adicionar o endereço quando o tipo do curso é presencial.

### Passos para Reproduzir
```
1. No site Beedoo QA Chalenge, clique em 'Cadastrar Cursos
2. Selecione o tipo de curso como 'Presencial'
3. Preencha os outros campos
4. Deixe o campo 'Endereço' em branco
5. Clique em Cadastrar Curso
6. Observe o erro retornado.
```
### Resultados esperados
```
A criação do curso deveria falhar e o usuário deveria receber uma mensagem dizendo que o endereço é obrigatório
```
### Prioridade e Severidade
```
 - Prioridade: Média
 - Severidade: Média
```

# Melhoria 001: Nenhum elemento do site Beedoo QA Chalenge possui ID

### Descrição:
No console do navegador é possível observar que nenhum elemento possui ID, dificultando possíveis automação de teste no futuro

### Passos para Reproduzir
```
1. No site Beedoo QA Chalenge, clique com o botão direito em qualquer lugar
2. Clique em 'Inspecionar elemento'
3. Selecione o campo 'Elements'
4. Pressione Ctrl+Shift+C e clique em qualquer elemento da tela
5. Observe que nenhum possui ID.
```
### Importância da melhoria
```
Caso os testes futuramente forem ser automatizados em um pipeline, a falta do ID dificultaria bastante o mapeamento dos elementos de front, necessitando de mais esforço e tempo do time de automação para otimizar a pipeline de testes.
```

# Melhoria 002: Criação de uma tela inicial

### Descrição:
No momento a tela inicial do Beedoo QA Chalenge é a funcionalidade de 'Listar Cursos' tornando inútil ter essa funcionalidade no topo do site ao lado de 'Cadastrar Curso'

### Importância da melhoria
```
A melhoria traría mais valor para a funcionalidade de 'Listar Cursos' além de fazer com que o site esteja mais nos padrões esperados do mercado
```