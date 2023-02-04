<div align="center">
<h2>Estudando MySQL 🐬</h2>
<h3>Seção 13: Banco de Dados MySQL</h3>
<p>Curso Desenvolvimento Web Completo 2022</p>
</div>

<div align="justify">

## Conteúdo

<a href="#aula01">Aula 01: O que é MySQL?</a><br>
<a href="#aula02">Aula 02: Um pouco mais sobre SQL.</a><br>
<a href="#aula03">Aula 03: Utilizando o PHPMyAdmin para manipulação do MySQL.</a><br>
<a href="#aula04">Aula 04: Criando e excluindo Bancos de Dados.</a><br>
<a href="#aula05">Aula 05: Tabelas e tipos de dados parte 1 - Um pouco de teoria.</a><br>
<a href="#aula06">Aula 06: Tabelas e tipos de dados parte 2 - Partindo para prática.</a><br>
<a href="#aula07">Aula 07: Extra - Entendendo a diferença entre os tipos de dados char e varchar.</a><br>
<a href="#aula08">Aula 08: Editando nome de tabelas.</a><br>
<a href="#aula09">Aula 09: Incluindo, editando e removendo colunas de tabelas.</a><br>
<a href="#aula10">Aula 10: .</a><br>


</div>

<hr>

<div id="aula01" align="center">
<h2>Aula 01: O que é MySQL?</h2>
</div>

É um `Sistema Gerenciador de Banco de Dados (SGBD)` Relacional, **gratuito**, que utiliza a **linguagem SQL** (Structured Query Language ou Linguagem de Consulta Estruturada) para **definir, manipular, controlar, transacionar e recuperar dados**.

Funciona como uma `interface entre as aplicações e os dados`, sendo o seu principal objetivo: controlar o acesso à manipulação e à organização dos dados persistido nos servidores de dados .

Basicamente, o SGBD fornece uma API para as aplicações, para que tenham acesso aos dados persistidos no servidor, sendo essa comunicação realizada entre as aplicações e o SGBD feita através da linguagem SQL!

Banco de Dados consistem em estruturas de dados organizadas em tabelas, que contém os registros, e esses registros estão relacionados entre essas tabelas.
  
<hr>

<div id="aula02" align="center">
<h2>Aula 02: Um pouco mais sobre SQL.</h2>
</div>

A `Linguagem SQL` é adotada como linguagem padrão nos principais BDs relacionais presentes no mercado, como MySQL, PostgreSQL, SQLServer e ORACLE. 

É a linguagem responsável por definir, manipular, controlar, transacionar e recuperar dados junto ao SGBD.

Pode ser dividida em cinco subcategorias e instruções com objetivos específicos:

1. DDL - Data Definition Language 
    - Linguagem de definição de dados. 
    - permite implementar a modelagem de dados - criar, alterar e remover estruturas de dados.

2. DML - Data Manipulation Language 
    - Linguagem de Manipulação de Dados.
    - Permite inclusão, alteração e remoção dos registros dentro das estruturas de dados.

3. DCL - Data Control Language 
    - Linguagem de Controle de Dados.
    - Possibilita gerenciar acesso por parte de usuários externos ao SGBD.

4. DTL - Data Transaction Language 
    - Linguagem de Transação de Dados.
    - Permite efetivar ou cancelar as transações junto ao SGBD.

5. DQL - Data Query Language 
    - Linguagem de Consulta de Dados 
    - permite recuperar dados através do estabelecimento de cláusulas, de operações lógicas, relacionais ou de funções de agragação.

<hr>

<div id="aula03" align="center">
<h2>Aula 03: Utilizando o PHPMyAdmin para manipulação do MySQL.</h2>
</div>

`PHPMyAdmin` é uma aplicação web, escrita em PHP, que serve para acessar e administrar o Banco de Dados MySQL. **É uma interface para o SGBD do MySQL**, acessada através do navegador/browser.

### Como acessar PHPMyAdmin?

1. Acessar o XAMPP.
2. Subir/startar o serviço do Apache (Start) - Porta 80.
3. Subir/startar o serviço do MySQL (Start) - Porta 3306.
4. Acessar no navegador: `localhost/phpmyadmin`.

### Apresentação do PHPMyAdmin:

- Na barra à esquerda, há a relação dos BDs existentes em nosso computador e gerenciado pelo SGBD do MySQL.
- À direita, informações a respito do servidor do BD e do servidor web, e alguns links para documentação e informações do PHPMyAdmin.

> No curso, trabalhamos com MariaDB, uma extensão do MySQL, uma branch open source!

<div id="aula04" align="center">
<h2>Aula 04: Criando e excluindo Bancos de Dados.</h2>
</div>

Bancos de dados são coleções organizadas de dados, que se relacionam de algum modo; consiste em agrupar registros de um domínio específico.

***Não existe um jeito certo e único de se criar um banco de dados***; depende do nível de abstração do assunto!

<br>

### No PHPMyAdmin:

Há duas formas de trabalho, disponíveis em qualquer client que se comunique com um SGBD:
1. instruções SQL.
2. através de interface gráfica.

<br>

### Instruções/Comandos SQL:

A) Para criar um BD (DDL): 

1. Comando `CREATE DATABASE nome_do_bd`. Exemplo:

~~~sql
CREATE DATABASE db_curso_web;
~~~

**Importante:** não utilizar caracteres especiais ou espaços quando for definir o nome do BD.

2. Clicar em Executar/Continuar.

<br>

B) Para remover um BD (DDL): 

1. Comando `DROP DATABASE nome_do_bd`. Exemplo:

~~~sql
DROP DATABASE db_curso_web;
~~~

2. Clicar em Executar/Continuar.

**Importante:** cuidado com os demais bancos de dados, porque contém informações importantes para o gerenciamento do próprio MySQL! Com exceção do banco de dados "test", evitar mexer nos demais BDs.

<br>

### Interface visual:

<br>

Para criar um BD:
1. Clicar em New/Novo.
2. Inserir o nome do BD.
3. Clicar em Criar.

Para excluir um BD:
1. Menu Operações.
2. Clicar em "Apagar a Base de Dados".

<div id="aula05" align="center">
<h2>Aula 05: Tabelas e tipos de dados parte 1 - Um pouco de teoria.</h2>
</div>

### Tabelas:

- Estruturas "semelhantes" a planilhas.
- Podem ser entendidas como unidades de armazenamento.
- São construídas com um número **finito de colunas**, e número **indefinido de linhas**!
- As informações cadastradas em aplicações são processados por uma linguagem de programação (como PHP) e, posteriormente, os dados processados podem ser inseridos como novos registros dentro de tabelas em BDs.
- São repositórios que qualificam os atributos de cada registro armazenado! Ou seja, além dos dados propriamente ditos de cada registro, associa metadados (como tipos e subtipos), que podem ser usados para controlar a integridade da informação ou otimizar pesquisas.

### Tipos de dados:

- Importantes para a definição de tabelas.
- Cada coluna de uma tabela é responsável pelo armazenamento de um tipo de dado específico, que deve ser definido no momento de criação da tabela!
- Exemplo:

<div align="center">
<img src="./assets/tipos_de_dados.png" width="70%">
</div>
<br>

- Alguns dos principais tipos de dados (e seus subtipos) são:

a) Campos de texto:

- `text`: tamanho variável que armazena uma grande quantidade de caracteres.
- `varchar`: tamanho variável que armazena de 0 até 255 caracteres (descrições textuais mais curtas).
- `char`: tamanho fixo que armazena de 0 até 255 caracteres.

b) Campos numéricos:

- `int`: valores numéricos inteiros, tanto positivos quanto negativos.
- `float`: valores numéricos fracionados, tanto positivos quanto negativos.

c) Campos de data e hora:

- `date`: data no formato YYYY/mm/dd.
- `time`: hora.
- `datetime`: combinação entre date e time em um mesmo campo.

> Indicar o tipo de campo corretamente permite trabalhar com funções nativas do SGBD!

<div id="aula06" align="center">
<h2>Aula 06: Tabelas e tipos de dados parte 2 - Partindo para prática.</h2>
</div>

Objetivo: criar uma tabela que receba registros de cursos (DDL).

Ao acessar o PHPMyAdmin, há duas opções para criar a tabela: através da interface visual ou da Linguagem SQL.

1. através da interface: 

- para criar uma tabela:
    - clicar no BD;
    - definir o nome da tabela;
    - inserir n°,. de colunas;
    - definir o nome de cada uma das colunas e os tipos de dados (**obs: none é o oposto de null**);
    - clicar em "Guardar".

- para remover uma tabela:
    - clicar sobre a tabela;
    - menu operações;
    - opção "delete the table".

<br>
2. através da linguagem SQL: 

- para criar uma tabela:

~~~sql
CREATE TABLE tb_cursos (
    id_curso int not null,
    imagem_curso varchar(100) not null,
    nome_curso char(50) not null,
    resumo text null,
    data_cadastro datetime not null,
    ativo boolean default true,
    investimento float(5, 2) default 0
);

/*float(n° dígitos, qtdd dígitos correspondentes à fração)*/
~~~

- para excluir uma tabela:

~~~sql
DROP TABLE tb_cursos;
~~~

<div id="aula07" align="center">
<h2>Aula 07: Extra - Entendendo a diferença entre os tipos de dados char e varchar.</h2>
</div>

1. CHAR:

- tamanho **fixo** em disco.
- todos os espaços relativos à quantidade de caracteres definidos ficam reservados no disco, independente de inserirmos ou não textos com este número de caracteres.
- vantagem: mais rápido para pesquisas.
- desvantagem: quanto mal utilizdo, pode reservar espaço em disco de forma desnecessária.

2. VARCHAR:

- tamanho **variável** em disco.
- possui a inteligência de reservar apenas a quantidade de caracteres utilizados para aquela string (ocupa menos espaço no BD).
- vantagem: por ser de tamanho variável, ocupa apenas o espaço necessário em disco.
- desvantagem: por ser de um tamanho variável, possui um metadado com uma instrução de finalização do texto, o que produz, em relação ao CHAR, maior lentidão em pesquisas.

Exemplo:
- Dado: MONICA
- Char (10 posições): M O N I C A _ _ _ _
- Varchar (10 posições): M O N I C A

<div id="aula08" align="center">
<h2>Aula 08: Editando nome de tabelas.</h2>
</div>

a) Utilizando recursos viduais:
- selecionar a tabela;
- clicar em operações;
- em "opções da tabela", na opção "renomeie a tabela para", inserir o novo nome;
- clicar em Executar/Continuar.

b) Intrução DDL do MySQL:
~~~sql
RENAME TABLE <nome_atual> TO <nome_novo>;
/* em seguida, atualizar a aplicação (botão Reload)!
~~~

<div id="aula09" align="center">
<h2>Aula 09: Incluindo, editando e removendo colunas de tabelas.</h2>
</div>

