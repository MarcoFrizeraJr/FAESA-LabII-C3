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

**DADOS DO SISTEMA**

Usuário:

* id
* nome
* cargo (Funcionário ou Gerente)

Produto:

* id
* nome
* quantidade em estoque
* quantidade mínima
* preço de custo
* preço de venda

Movimentação:

* id
* produto
* tipo (Entrada ou Saída)
* quantidade
* responsável
* data e hora

Solicitação de Reposição:

* id
* produto
* quantidade solicitada
* responsável pela solicitação
* status (Pendente, Aprovada ou Recusada)

**CONTAS DE USUÁRIO**

O sistema possuirá dois tipos de usuários: Funcionário e Gerente.
Os Funcionários poderão consultar produtos, registrar movimentações de entrada e saída e solicitar reposição de mercadorias.
Os Gerentes possuirão acesso completo ao sistema, podendo gerenciar produtos, usuários, aprovar reposições e corrigir movimentações realizadas incorretamente.
Somente os Gerentes poderão remover produtos cadastrados.

**CONTROLE DE ESTOQUE**

Toda movimentação de entrada aumentará automaticamente a quantidade disponível do produto.
Toda movimentação de saída reduzirá automaticamente a quantidade disponível do produto.
O sistema não permitirá registrar saídas superiores à quantidade disponível em estoque.
Produtos sem estoque disponível não poderão sofrer novas movimentações de saída.

**CONTROLE DE ESTOQUE MÍNIMO**

Cada produto possuirá uma quantidade mínima definida durante o cadastro.
Quando a quantidade disponível atingir ou ficar abaixo desse limite, o sistema classificará o produto como "Estoque Baixo".
Produtos classificados como "Estoque Baixo" gerarão automaticamente uma solicitação de reposição pendente.

**PROCESSO DE REPOSIÇÃO**

As solicitações de reposição poderão ser criadas automaticamente pelo sistema ou manualmente pelos Funcionários.
Toda solicitação deverá ser analisada por um Gerente.
Somente após a aprovação da solicitação será permitida a entrada da nova mercadoria no estoque.
Solicitações recusadas permanecerão registradas para fins de auditoria.

**GERENCIAMENTO DE MOVIMENTAÇÕES**

Toda movimentação deverá armazenar o usuário responsável e a data da operação.
Movimentações não poderão ser excluídas diretamente.
Caso uma movimentação tenha sido registrada incorretamente, o sistema realizará uma movimentação inversa para corrigir o estoque, preservando o histórico das operações.
Somente Gerentes poderão autorizar correções.

**RELATÓRIOS**

O sistema permitirá a geração de relatórios contendo:
* Produtos em estoque;
* Produtos com estoque baixo;
* Histórico de movimentações;
* Produtos mais movimentados;
* Solicitações de reposição pendentes.

**SALVAMENTO DOS DADOS**

Os dados serão gravados automaticamente em arquivos de texto (.txt) após:

* Cadastro de produto;
* Alteração de produto;
* Exclusão de produto;
* Cadastro de usuário;
* Registro de movimentação;
* Criação de solicitação de reposição;
* Aprovação ou recusa de solicitação;
* Correção de movimentações.

Ao iniciar o sistema, todas as informações serão carregadas dos arquivos para a memória da aplicação.



### Organização das Tarefas

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
