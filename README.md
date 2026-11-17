📚 Revisão de Banco de Dados
📌 Sobre o projeto

Este repositório foi desenvolvido com o objetivo de praticar e revisar conceitos fundamentais de Banco de Dados utilizando SQL Server.

O projeto apresenta a estrutura de um banco de dados para gerenciamento de uma livraria, permitindo compreender como organizar informações, criar tabelas, estabelecer relacionamentos entre entidades e manipular registros por meio de comandos SQL.

O desenvolvimento aborda conceitos importantes para quem está iniciando os estudos em Banco de Dados ou deseja reforçar seus conhecimentos na linguagem SQL.

🎯 Objetivos
Praticar a criação de bancos de dados utilizando SQL.
Compreender a criação e estruturação de tabelas.
Aplicar chaves primárias e estrangeiras.
Entender os relacionamentos entre tabelas.
Praticar a inserção de registros utilizando INSERT INTO.
Realizar consultas utilizando SELECT.
Compreender a organização de um banco de dados relacional.
🛠️ Tecnologias utilizadas
SQL Server: Sistema de gerenciamento de banco de dados utilizado para executar os comandos SQL.
SQL: Linguagem utilizada para criação, manipulação e consulta de dados.
Git e GitHub: Ferramentas utilizadas para versionamento e armazenamento do projeto.
📂 Estrutura do projeto
text
Revisao-BD/
│
├── README.md
│
└── livraria.sql

Arquivos do projeto

livraria.sql

Arquivo principal do projeto, contendo os comandos SQL responsáveis pela criação do banco de dados, definição das tabelas, inserção de registros fictícios e realização de consultas.

README.md

Arquivo de documentação que apresenta o projeto, seus objetivos, tecnologias utilizadas e instruções para execução.

🗄️ Estrutura do banco de dados

O banco de dados utilizado no projeto recebe o nome de db_livraria.

Ele foi organizado em sete tabelas, cada uma responsável por armazenar informações específicas do sistema.

1. tbl_editora

Armazena os dados das editoras responsáveis pela publicação dos livros.

Campo	Descrição
ID_Editora	Identificador único da editora
NomeEmpresa	Nome da empresa
TelefoneContato	Telefone para contato
EmailCorporativo	E-mail corporativo
2. tbl_autor

Armazena as informações dos autores cadastrados.

Campo	Descrição
ID_Autor	Identificador único do autor
NomeCompleto	Nome completo do autor
Nacionalidade	Nacionalidade do autor
DataNascimento	Data de nascimento
3. tbl_cliente

Armazena os dados dos clientes da livraria.

Campo	Descrição
ID_Cliente	Identificador único do cliente
NomeCompleto	Nome completo do cliente
Email	E-mail do cliente
CPF	Documento de identificação
DataCadastro	Data de cadastro do cliente
4. tbl_livro

Armazena as informações dos livros disponíveis na livraria.

Campo	Descrição
ISBN	Código identificador do livro
Titulo	Título do livro
PrecoVendaAtual	Preço atual de venda
QtdEstoque	Quantidade disponível no estoque
AnoPublicacao	Ano de publicação
ID_Editora	Identificador da editora responsável
5. tbl_livro_autor

Responsável por relacionar livros e autores.

Essa tabela permite representar o relacionamento entre livros e autores, considerando que um livro pode possuir mais de um autor e um autor pode escrever vários livros.

Campo	Descrição
ISBN	Identificador do livro
ID_Autor	Identificador do autor

A tabela utiliza uma chave primária composta pelos campos ISBN e ID_Autor.

6. tbl_pedido

Armazena os pedidos realizados pelos clientes.

Campo	Descrição
ID_Pedido	Identificador único do pedido
DataHora	Data e horário do pedido
ValorTotal	Valor total da compra
ID_Cliente	Identificador do cliente responsável pelo pedido
7. tbl_item_pedido

Armazena os livros associados a cada pedido.

Campo	Descrição
ID_ItemPedido	Identificador do item do pedido
Quantidade	Quantidade de livros comprados
PrecoUnitarioVenda	Preço unitário no momento da venda
ID_Pedido	Identificador do pedido
ISBN	Identificador do livro
🔗 Relacionamentos entre as tabelas

O banco de dados utiliza chaves primárias e estrangeiras para estabelecer relacionamentos entre as tabelas.

Os principais relacionamentos são:

Editora e Livro: uma editora pode possuir vários livros cadastrados.
Livro e Autor: relacionamento de muitos para muitos, realizado pela tabela intermediária tbl_livro_autor.
Cliente e Pedido: um cliente pode realizar vários pedidos.
Pedido e Item do Pedido: um pedido pode possuir vários itens.
Livro e Item do Pedido: um livro pode aparecer em vários itens de pedidos diferentes.

Esses relacionamentos ajudam a manter a organização e a integridade das informações armazenadas.

▶️ Como executar o projeto

Para executar o projeto, siga as etapas abaixo:

Pré-requisitos
Ter o Microsoft SQL Server instalado.
Possuir o SQL Server Management Studio (SSMS) ou outra ferramenta compatível para executar comandos SQL.
Passo 1 — Clonar o repositório

Abra o terminal e execute:

bash
git clone https://github.com/Vitinho2210/Revisao-BD.git

Passo 2 — Acessar a pasta
bash
cd Revisao-BD

Passo 3 — Abrir o arquivo SQL

Abra o SQL Server Management Studio e conecte-se à sua instância do SQL Server.

Em seguida, abra o arquivo:

text
livraria.sql

Passo 4 — Executar os comandos

Execute o script para criar o banco de dados, construir as tabelas e inserir os registros.

Atenção: o script possui relacionamentos com chaves estrangeiras. É necessário garantir que os registros referenciados existam antes de inserir os dados nas tabelas dependentes. Alguns registros de exemplo presentes nas inserções de autores e livros precisam ser revisados para manter a integridade referencial.

🔎 Consultas SQL

Ao final do arquivo SQL, são utilizadas consultas SELECT para visualizar os registros armazenados nas tabelas.

Exemplo:

sql
SELECT * FROM tbl_editora;

SELECT * FROM tbl_cliente;

SELECT * FROM tbl_autor;

SELECT * FROM tbl_livro;

SELECT * FROM tbl_livro_autor;

SELECT * FROM tbl_pedido;

SELECT * FROM tbl_item_pedido;


O comando SELECT permite consultar e visualizar os dados armazenados no banco de dados.

📖 Conceitos praticados

Durante o desenvolvimento deste projeto, são trabalhados os seguintes conceitos:

Banco de dados relacionais.
Criação de banco de dados com CREATE DATABASE.
Seleção de banco de dados com USE.
Criação de tabelas com CREATE TABLE.
Chaves primárias com PRIMARY KEY.
Chaves estrangeiras com FOREIGN KEY.
Restrições de integridade com UNIQUE, NOT NULL e CHECK.
Inserção de registros com INSERT INTO.
Consulta de informações com SELECT.
Relacionamentos entre entidades.
👨‍💻 Autor

Vitinho2210

GitHub: https://github.com/Vitinho2210

📄 Licença

Este projeto possui finalidade educacional e foi desenvolvido para prática e revisão de conceitos de Banco de Dados.
