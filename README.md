### **Trabalho prático de Laboratório de Programação II — Conceito 3. Grupo de desenvolvimento:** 

- ARTHUR EVANGELISTA OLIVEIRA 
- ENZO PAVAO MADUREIRA DA SILVA 
- JOÃO VITOR GERA BOF 
- MARCO ANTONIO FRIZERA JUNIOR 
- TARSICIO ANTONIO DE LIMA

### **Sistema de Controle de Estoque para Pequeno Comércio**

O Sistema de Controle de Estoque para Pequeno Comércio tem como objetivo auxiliar pequenos estabelecimentos no gerenciamento de seus produtos, permitindo o controle eficiente da entrada, saída e consulta de itens em estoque.

O sistema será utilizado por proprietários e funcionários responsáveis pelo controle dos produtos comercializados. Por meio dele, será possível cadastrar produtos, consultar informações, atualizar quantidades disponíveis e registrar movimentações de entrada e saída de mercadorias.

### **Funcionalidades Principais**

- Cadastro de produtos;
- Consulta de produtos cadastrados;
- Atualização de informações dos produtos;
- Registro de entrada de mercadorias;
- Registro de saída de mercadorias;
- Consulta da quantidade disponível em estoque;
- Geração de relatórios simples do estoque;
- Armazenamento dos dados em arquivo;
- Benefícios;
- Melhor organização do estoque;
- Redução de perdas por falta de controle;
- Facilidade na consulta de produtos;
- Agilidade na administração do comércio.

### **Regras de Negócio**

1. Cada produto deve possuir um código único.
2. Não é permitido cadastrar produtos com preço menor ou igual a zero.
3. Não é permitido cadastrar produtos com quantidade inicial negativa.
4. A entrada de estoque deve aumentar a quantidade disponível do produto.
5. A saída de estoque só pode ser realizada se houver quantidade suficiente disponível.
6. O sistema não deve permitir que o estoque fique negativo.
7. Produtos perecíveis devem possuir uma data de validade válida.
8. Não é permitido excluir um produto que possua movimentações registradas.
9. Toda movimentação de entrada ou saída deve ser registrada em arquivo.
10. O sistema deve emitir um alerta quando a quantidade de um produto estiver abaixo do estoque mínimo definido.

### Organização das Tarefas (Trello)

**Etapa 1 – Planejamento**

- Definição dos requisitos do sistema;
- Levantamento das funcionalidades;
- Criação da descrição do projeto.

**Etapa 2 – Modelagem**

- Desenvolvimento do diagrama de classes UML;
- Definição dos atributos e métodos das classes;
- Organização dos pacotes.

**Etapa 3 – Desenvolvimento**

- Implementação da classe Produto;
- Implementação da classe Estoque;
- Implementação da classe de movimentação;
- Implementação do menu principal;
- Implementação da persistência em arquivos.

**Etapa 4 – Testes**

- Testes de cadastro;
- Testes de entrada e saída de produtos;
- Testes de gravação e leitura dos arquivos;
- Correção de erros.

**Etapa 5 – Documentação**

- Elaboração do relatório;
- Captura de telas;
- Revisão do código.

**Etapa 6 – Apresentação**

- Preparação dos slides;
- Demonstração do sistema.

### Possíveis Classes

**1. Produto**

- código
- nome
- preço
- quantidade

**2. ProdutoPerecivel**

- dataValidade

**3. Estoque**

- lista de produtos
- cadastrarProduto()
- removerProduto()
- buscarProduto()

**4. Movimentacao**

- entradaProduto()
- saidaProduto()
