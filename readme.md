<div align="center">
<a href="https://github.com/monicaquintal" target="_blank"><img align="right" height="130" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" /></a>
<h2>Estudando MySQL</h2>
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
<a href="#aula10">Aula 10: INSERT - Inserindo dados em tabela.</a><br>
<a href="#aula11">Aula 11: SELECT - Consultando dados.</a><br>
<a href="#aula12">Aula 12: Filtrando registros (WHERE).</a><br>
<a href="#aula13">Aula 13: Populando o banco de dados com registros para testes.</a><br>
<a href="#aula14">Aula 14: SELECT - Filtros com Operadores de Comparação.</a><br>
<a href="#aula15">Aula 15: SELECT - Filtros com Operadores Lógicos.</a><br>
<a href="#aula16">Aula 16: SELECT - Filtros com o operador BETWEEN.</a><br>
<a href="#aula17">Aula 17: SELECT - Filtros com o operador IN.</a><br>
<a href="#aula18">Aula 18: SELECT - Filtros com o operador LIKE.</a><br>
<a href="#aula19">Aula 19: SELECT - Ordenando resultado.</a><br>
<a href="#aula20">Aula 20: SELECT - Limitando retorno.</a><br>
<a href="#aula21">Aula 21: SELECT - Funções de agregação parte 1: MAX, MIN e AVG.</a><br>
<a href="#aula22">Aula 22: SELECT - Funções de agregação parte 2: SUM e COUNT.</a><br>
<a href="#aula23">Aula 23: SELECT - Agrupando seleção de registros (GROUP BY).</a><br>
<a href="#aula24">Aula 24: SELECT - Filtrando seleções agrupadas (HAVING).</a><br>
<a href="#aula25">Aula 25: UPDATE - Atualizando registros.</a><br>
<a href="#aula26">Aula 26: DELETE - Excluindo registros.</a><br>
<a href="#aula27">Aula 27: Introdução ao relacionamento entre tabelas, chave primária e estrangeira.</a><br>

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

### 1. Através da interface visual:

a) Incluindo colunas:
- clicar no botão que expande os recursos da tabela.
- expendir as opções de colunas.
- clicar em "New".
- inserir os dados da nova Coluna.
- clicar em Guardar.

b) Editando a coluna:
- clicar no nome da tabela;
- em Estrutura, clicar na opção "Muda" da coluna que queremos alterar (ou diretamente pela lista de colunas no menu esquerdo);
- fazer a alteração e clicar em "Guardar".

c) Deletando coluna:
- clicar no nome da tabela;
- em Estrutura, clicar na opção "Eliminar" da coluna que queremos excluir (ou diretamente pela lista de colunas no menu esquerdo);
- clicar em Ok.

<br>

### 2. Linguagem SQL:

Sintaxe:
~~~sql
ALTER TABLE <comando>;
~~~

- `ADD`: permite a inclusão de uma nova coluna em uma tabela.
- `CHANGE`: permite a alteração do nome de uma coluna e de suas propriedades, como o tipo.
- `DROP`: permite a remoção de uma coluna da tabela.

a) Inclusão de coluna:

~~~sql
ALTER TABLE nome_da_tabela ADD COLUMN nome_da_coluna <TIPO_DE_DADO> <PARÂMETRO>;
~~~

b) Alteração de coluna:

~~~sql
ALTER TABLE nome_da_tabela CHANGE nome_da_coluna <DADOS_A_SEREM_MODIFICADOS>;

/* caso queira modificar o nome: */
ALTER TABLE nome_da_tabela CHANGE nome_antigo_da_coluna novo_nome_da_coluna <DEMAIS_DADOS_A_MODIFICAR>;

/* caso queira manter o nome: */
ALTER TABLE nome_da_tabela CHANGE nome_da_coluna nome_da_coluna <DADOS_A_SEREM_MODIFICADOS>;

/* se mudarmos apenas o nome, ainda assim devemos indicar o tipo na sequência, sem precisas do parâmetro!*/
~~~

c) Exclusão de coluna:

~~~sql
ALTER TABLE nome_da_tabela DROP nome_da_coluna;
~~~

<div id="aula10" align="center">
<h2>Aula 10: INSERT - Inserindo dados em tabela.</h2>
</div>

### 1. Através da interface visual:
- clicar no BD e tabela desejados;
- clicar em "Inserir";
- preencher o formulário com os dados;
- clicar em "Executar".
- clicando na tabela, poderemos verificar os registros realizados.

<br>

### 2. Linguagem SQL:

~~~sql
INSERT INTO nome_da_tabela (coluna1, coluna2, coluna3) VALUES (valor_col1, valor_col2, valor_col3);
~~~

<div id="aula11" align="center">
<h2>Aula 11: SELECT - Consultando dados.</h2>
</div>

Como recuperar os registros inseridos? (DML)

### 1. Através da interface visual:
- basta clicar sobre a tabela!

<br>

### 2. Linguagem SQL:

~~~sql
SELECT <colunas> FROM <tabela>;
~~~

Podemos utilizar o `caractere coringa: *` para selecionar todos os campos da tabela, como a seguir:

~~~sql
SELECT * FROM <tabela>;
~~~

Atentar-se ao tamanho do BD e quantidade de dados antes de utiliza-lo - verificar se vale a pena!

<div id="aula12" align="center">
<h2>Aula 12: Filtrando registros (WHERE).</h2>
</div>

Como utilizar filtros para limitar as consultas, atualizações e remoções de registros?
- filtros permitem especificar o que queremos obter em um BD, especificam quais condições devem ser satisfeitas.
- também permitem transformar uma relação de registros em informação!

Exemplo:

~~~sql
SELECT <coluna> FROM <tabela> WHERE <condição>;

/* Caso queira selecionar mais ade uma coluna: */
SELECT <colunas> FROM <tabela> WHERE <condição> AND <condição>;
~~~

***Importante:***

a) Operadores de comparação:

<div align="center">

Operador | Função
---------|---------
= | Valor da esquerda igual ao da direita
&lt; | Valor da esquerda menor que o da direita
&lt;= | Valor da esquerda menor ou igual ao da direita
&gt; | Valor da esquerda maior que o da direita
&lt;= | Valor da esquerda maior ou igual ao da direita

</div>

b) Operadores lógicos:

<div align="center">

Operador | Função
---------|---------
AND | Todas as operações de comparação devem ser verdadeiras
OR | Pelo menos 1 das condições de operação deve ser verdadeira.

</div>

<div id="aula13" align="center">
<h2>Aula 13: Populando o banco de dados com registros para testes.</h2>
</div>

Para preencher o BD demonstrado em aula, o prof. gerou dados aleatórios através do site [Generate Data](https://generatedata.com/).

E, para inserir diversos dados simultaneamente, exemplo:

~~~sql
INSERT INTO `tabela` (`col1`,`col2`,`col3`) VALUES (1,"Jorden",47), (2,"Lacey",59), (3,"Lillith",48);
/* syntax sugar*/
~~~

Obs: "syntax sugar" = sintaxe dentro da linguagem que tem por finalidade tornar suas construções mais fáceis de serem lidas e expressas.

<div id="aula14" align="center">
<h2>Aula 14: SELECT - Filtros com Operadores de Comparação.</h2>
</div>

Como consultar os registros dentro das tabelas de forma mais avançada? Utilizar operadores de comparação para filtrar registros!

***Operar apenas com linguagem SQL*** (geralmente não há recursos de seleção avançada através da interface visual)!

### Exemplo:

~~~sql
SELECT
  id_curso, nome_curso 
FROM 
  `tb_cursos` 
WHERE 
  investimento < 500.00;
~~~

### Operadores de Comparação

<div align="center">

Operadores | Função
:---------:|---------
= | Valor da esquerda igual ao valor da direita
&lt; | Valor da esquerda menor que o valor da direita
&lt;= | Valor da esquerda menor ou igual ao valor da direita
&gt; | Valor da esquerda maior que o valor da direita
&gt;= | Valor da esquerda maior ou igual ao valor da direita

</div>

<div id="aula15" align="center">
<h2>Aula 15: SELECT - Filtros com Operadores Lógicos.</h2>
</div>

Operadores lógicos combinam resultados de operadores de comparação.

### Operadores Lógicos

<div align="center">

Operadores | Função
:---------:|---------
AND | Todas as operações de comparação devem ser verdadeiras
OR | Pelo menos uma das operações de comparação deve ser verdadeira

</div>

### Exemplo:

~~~sql
SELECT
	* 
FROM 
	`tb_alunos` 
WHERE 
	interesse = 'Jogos' AND idade >= 30;
~~~

<div id="aula16" align="center">
<h2>Aula 16: SELECT - Filtros com o operador BETWEEN.</h2>
</div>

O operador `BETWEEN` é utilizado quando precisamos filtrar registros cujo valor de determinada coluna encontra-se em um intervalo específico (number ou date).

~~~sql
SELECT
	* 
FROM 
	`tb_alunos` 
WHERE 
	idade BETWEEN  18 AND 21;
~~~

<div id="aula17" align="center">
<h2>Aula 17: SELECT - Filtros com o operador IN.</h2>
</div>

O operador `IN` é utilizado para filtrar registros com base na especificação de uma lista de possibilidades.

Exemplo:

~~~sql
SELECT
	* 
FROM 
	`tb_alunos` 
WHERE 
	interesse = 'Jogos' OR interesse = 'Música' OR interesse = 'Esportes';

/* utilizando o operador IN: */

SELECT
	* 
FROM 
	`tb_alunos` 
WHERE 
	interesse IN ('Jogos', 'Música', 'Esportes');
~~~

Há também a possibilidade de utilizar `NOT IN`:

~~~sql
SELECT
	* 
FROM 
	`tb_alunos` 
WHERE 
	interesse NOT IN ('Jogos', 'Música', 'Esportes');
~~~

<div id="aula18" align="center">
<h2>Aula 18: SELECT - Filtros com o operador LIKE.</h2>
</div>

O operador `LIKE` permite realizar filtros com base em uma pesquisa de um conjunto de caracteres dentro de uma coluna textual.

O operador LIKE travalha com dois caracteres coringas:
- `%`: indica que pode haver a existência de qualquer conjunto de caracteres no texto.
- `_`: indica que pode haver um ou mais caracteres em uma posição específica do texto. É mais exato que o %, pois refere-se a uma posição definida!

Podemos combinar os dois coringas também!

Exemplo:

~~~sql
SELECT
	* 
FROM 
	`tb_alunos` 
WHERE 
	nome = 'Evelyn';
~~~

Aplicando o operador IN:

~~~sql
SELECT
	* 
FROM 
	`tb_alunos` 
WHERE 
	nome LIKE 'Evelyn';
~~~

Utilizando caracteres coringa:

~~~sql
SELECT * FROM `tb_alunos`: 

WHERE 
  nome LIKE '%e';
/* qualquer conjunto de caracteres que finalize com a letra E */

WHERE
  nome LIKE '%a%';
/* pesquisa ocorrência do char "a", começando e terminando com qqr caractere */

WHERE
  nome LIKE '_riel';
/* pesquisa palavra com UM caractere desconhecido à esq. */

WHERE
  nome LIKE 'I__';
/* pesquisa palavra que inicia com I e tem 2 caracteres indef. à dir. */
~~~


<div id="aula19" align="center">
<h2>Aula 19: SELECT - Ordenando resultado.</h2>
</div>

Como podemos ordenar os resultados das consultas? Utilizaremos a instrução/palavra reservada `ORDER BY`.

A construção de uma query (consulta) possui uma estrutura, como representado a seguir:

~~~sql
SELECT
  <coluna(s)>
FROM
  <tabela(s)>
WHERE /* opcional */
  <filtro(s)>
ORDER BY /* opcional */
  <categoria1> ASC, <categoria2> DESC;
~~~

Sendo os pivôs de ordenação de resultados:

- `ASC`: Ascending (ascendente). É o default, caso não coloquemos a informação de ASC ou DESC!
- `DESC`: Descending (descendente).

<div id="aula20" align="center">
<h2>Aula 20: SELECT - Limitando retorno.</h2>
</div>

 O `LIMIT` é um recurso que limita a quantidade de registros informados, no momento de retorno da consulta; é geralmente usado quando há muitos registros e queremos limitar a quantidade de registros que serão exibidos ao usuário final, como em paginações.

Exemplo da aplicação:

~~~sql
SELECT
  <coluna(s)>
FROM
  <tabela(s)>
WHERE
  <filtro(s)>
ORDER BY 
  <ordenação>
LIMIT 
  5
OFFSET
  2 
~~~

Importante:

- o `LIMIT` é opcional; coloca-lo sempre ao final da query!
- o `OFFSET` pode ser usado apenas quando o LIMIT é declarado (depende dele, embora também seja opcional)! Ele funciona como um deslocamento, podendo ser definido de 2 formas:

~~~sql
<...>
LIMIT 
  5
OFFSET
  2 
~~~

ou: 

~~~sql
<...>
LIMIT
    2, 5
/* 2 = OFFSET e 5 = LIMIT */
/* SINTAXE: VALOR_OFFSET, VALOR_LIMIT*/
~~~

Quando definimos o ***OFFSET***, serão retornados os registros a partir de seu valor:
- Exemplo: em OFFSET = 4, retornará os dados a partir do 4° registro - incluindo o valor do 4° registro)!
- É MUITO IMPORTANTE lembrar que, no BD, o primeiro registro ocupará a posição 0 (zero)!

<div id="aula21" align="center">
<h2>Aula 21: SELECT - Funções de agregação parte 1: MAX, MIN e AVG.</h2>
</div>

Resolvem problemas que são corriqueiros no dia-a-dia.

Sintaxe:

~~~sql
SELECT
  <funções_de_agregação>
FROM
  <tabela(s)>
WHERE
  <filtro(s)>
~~~ 

Sendo:

1. `MIN(<coluna>)`: retorna o **menor** valor de todos os registros com base em uma coluna.

2. `MAX(<coluna>)`: retorna o **maior** valor de todos os registros com base em uma coluna.

3. `AVG(<coluna>)`: retorna a **média** de todos os registros com base em uma coluna.

> A operação `TRUNCATE <tabela>` limpa todos os registros existentes dentro da tabela!!!

<div id="aula22" align="center">
<h2>Aula 22: SELECT - Funções de agregação parte 2: SUM e COUNT.</h2>
</div>

Sintaxe:

~~~sql
SELECT
  <funções_de_agregação>
FROM
  <tabela(s)>
WHERE
  <filtro(s)>
~~~ 

Sendo:

1. `SUM(<coluna>)`: retorna a **soma** dos valores de todos os registros com base em uma coluna.

2. `COUNT(*)`: retorna a **quantidade** de todos os registros de uma tabela.

<div id="aula23" align="center">
<h2>Aula 23: SELECT - Agrupando seleção de registros (GROUP BY).</h2>
</div>

A instrução `GROUP BY` agrupa os registros com base em uma ou mais colunas cujos valores sejam iguais. Permite realizar funções de agregação em cada subconjunto agrupado de registros. 

É muito utilizado em conjunto com funções de agregação!

Está posicionado em um local espefífico da construção da query (após FROM ou WHERE, e sempre antes de ORDER BY E LIMIT, quando utilizados).

Sintaxe:

~~~sql
SELECT
  <coluna(s)>
FROM
  <tabela(s)>
WHERE
  <filtro(s)>
GROUP BY
 <agrupamento>
ORDER BY 
  <ordenação>
LIMIT
  <offset>, <limit>
~~~ 

<div id="aula24" align="center">
<h2>Aula 24: SELECT - Filtrando seleções agrupadas (HAVING).</h2>
</div>

A instrução `HAVING` serve para aplicar filtros aos resultados de colunas agrupadas (HAVING não vive sem  GROUP BY, mas o contrário não é obrigatório!)!

Sintaxe:

~~~sql
SELECT
  <coluna(s)>
FROM
  <tabela(s)>
WHERE
  <filtro(s)>
GROUP BY
 <agrupamento>
HAVING
  <filtros_sobre_resultado_do_agrupamento>
ORDER BY 
  <ordenação>
LIMIT
  <offset>, <limit>
~~~ 

Observação: no MySQL podemos utilizar `!=` ou `<>` para indicar "diferente".

<div id="aula25" align="center">
<h2>Aula 25: UPDATE - Atualizando registros.</h2>
</div>

Como atualizar registros contidos dentro de tabelas em nossos BDs?

A instrução `UPDATE` faz parte do DML, ou seja, instrução de manipulação de dados.

~~~sql
UPDATE
  <tabela>
SET
  <coluna> = <valor> , <coluna> = <valor>
WHERE
  <filtro(s)>
~~~

O **WHERE** especifica qual o registro ou conjunto de registros que serão afetados pela instrução de atualização!

<div id="aula26" align="center">
<h2>Aula 26: DELETE - Excluindo registros.</h2>
</div>

A instrução `DELETE` faz parte do subconjunto de instruções DML, ou seja, mais um comando para manipulação de dados.

Sintaxe:

~~~sql
DELETE FROM
  <tabela>
WHERE
  <filtro(s)>
~~~

> ***IMPORTANTE:*** caso o WHERE seja omitido (não esteja presente no comando DELETE), ***TODOS*** os registros da tabela serão removidos!!!

Caso tenha dúvidas sobre quais registros serão afetados pelo DELETE, podemos ***simular a pesquisa*** clicando no botão na parte inferior da tela!!!

Um detalhe interessante é que geralmente os registros não são removidos. Normalmente, opta-se por fazer a atualização no registro, modificando alguma coluna que indique seu estado (ativo/inativo). Geralmente são mantidos para fins de log/histórico.

<div id="aula27" align="center">
<h2>Aula 27: Introdução ao relacionamento entre tabelas, chave primária e estrangeira.</h2>
</div>

O `relacionamento entre tabelas` consiste em tentar imitar a relação entre as coisas que existem no mundo real.

Há ***três tipos*** de relacionamentos possíveis entre tabelas:

- um para um:
- um para muitos:
- muitos para muitos: 

A `chave primária` serve como identificador único para cada registro de uma tabela, de modo que esse identificador não se repita em momento algum para nenhum outro registro. 
- É muito utilizada para seleção, atualização, remoção de registros e criação de relacionamentos consistentes entre tabelas. 
- Pode ser uma chave composta, quando é composta por 2 ou mais campos.

Já a `chave estrangeira`, é uma referência à chave primária de outra tabela! 