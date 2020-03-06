# wiki

# MySQL
MySQL é um dos **Sistemas de Gerenciamento de Bancos de Dados(DBMS)** mais utilizados em todo mundo, ele utiliza a **SQL** ou **Structured Query Language**, ou **Linguagem de Consulta Estruturada** que é a linguagem de pesquisa declarativa padrão para **banco de dados relacional**.



### Algumas coisas para serem lembradas:

- **Comandos do cliente** (por exemplo, *help*, *quit*, e *clear*) e **palavras chave do SQL** (por exemplo, `SELECT`, `CREATE TABLE`, e `INSERT`) são **case-insensitive** (não são influenciados por letras maiúsculas ou minusculas).
- **Nomes de colunas** são **case-sensitive** (sofrem influência de letras maiúsculas e minusculas).
- **Nomes de tabelas** sao **case-sensitive** na maioria das **plataformas Unix**, mas **case-insensitive** em **plataformas Windows**.
> No geral, é uma boa ideia tratar **todos os identificadores** (nomes de bancos, colunas, tabelas, etc.) e **STRINGS como case-sensitive**. 
- Você pode **digitar suas instruções SQL em mútiplas linhas** pressionando *Enter* no meio dela.
- Utilizar um **ponto e vírgula**( ; ) seguido de um *Enter* **encerra** a instrução SQL **e a manda para execução** no servidor.

## Comandos básicos MySQL

### Mostrar bancos de dados existentes:
- Use a instrução `SHOW DATABASES`:

![show.png](/show.png)


### Criar um novo banco de dados:
- Use a instrução `CREATE DATABASE` + ***nome do banco***:

![create.png](/create.png)

> Você pode utilizar a instrução `SHOW DATABASES` novamente para confirmar a criação.

### Criar uma tabela dentro de um banco de dados:
- Primeiro você deve **acessar o banco de dados no qual deseja criar** a tabela. Para isso utilize a instrução **`USE` + *nome do banco***.

![use.png](/use.png)
> A instrução `USE` informa o MySQL para **usar a tabela escolhida como padrão para as próximas instruções**.
- Agora crie a tabela com a instrução `CREATE TABLE` + ***nome da tabela***:

![createtable.png](/createtable.png)

> A **tipagem de dados** e **primary key** devem sempre ser especificados. 

### Mostrar as tabelas existentes no banco de dados que está em uso:

- Use a instrução `SHOW TABLES`:

![showtables.png](/showtables.png)

---
- Você pode utilizar a instrução `DESCRIBE` + ***nome da tabela*** para **mostrar as informações de todas as colunas** da tabela:

![describe.png](/describe.png)

### Inserir dados em uma tabela:
- Pode ser feito utilizando a instrução `INSERT...VALUES`:

```
  INSERT INTO nome_tabela ( coluna1, coluna2, coluna3) VALUES
  	( dado_column1, dado_column2, dado_column3 ),
  	( dado2_column1, dado2_column2, dado2_column3 ),
  	( dado3_column1, dado3_column2, dado3_column3 );
```
![insert.png](/insert.png)

### Recuperar registros da tabela:
- Use a instrução `SELECT`...`FROM` + ***nome da tabela***

> Em SQL " * " (asterísco) é usado para referênciar **"tudo possível"** existente no ambiente trabalhado.

![select.png](/select.png)

> No exemplo acima lê-se: `SELECIONE` *TODAS COLUNAS* `DE` cats (tabela).

#### Recuperar registros de coluna e linha específica usando a condição `WHERE`:

``` 
SELECT nome_coluna FROM nome_tabela WHERE condição = true;
```

![selectwhere.png](/selectwhere.png)

### Deletar registro de uma tabela

- Use a instrução `DELETE` utilizando `WHERE` para específicar o que será deletado:

![delete.png](/delete.png)

### Adicionar ou deletar uma coluna de uma tabela:

- Use a instrução `ALTER TABLE` + *nome da tabela* para fazer alterações em uma tabela.

##### ADD

- Use a intrução `ALTER TABLE ... ADD` para adicionar uma nova coluna na tabela específicada.
```
	ALTER TABLE nome_tabela ADD nome_nova_coluna data_type;
```
> Você pode utilizar a instrução `AFTER` para especificar a posição onde a nova coluna será criada.

![alteradd.png](/alteradd.png)

**Resultado:**

![describeadd.png](/describeadd.png)

#### DROP

- Use a instrução `ALTER TABLE ... DROP` para deletar uma coluna da tabela específicada.

```
	ALTER TABLE nome_tabela DROP nome_coluna;
```

![alterdrop.png](/alterdrop.png)

**Para você treinar:**
- [APP - Sololearn - aulas e exercícios](https://play.google.com/store/apps/details?id=com.sololearn)
- [ SQL Quiz](https://www.w3schools.com/quiztest/quiztest.asp?qtest=SQL)
- [ SQL Exercícios ](https://www.w3schools.com/sql/sql_exercises.asp)

Referência:
- [Site Oficial](https://dev.mysql.com/doc/mysql-getting-started/en/#mysql-getting-started-basic-ops).
- [SQL Tutorial W3Schools](https://www.w3schools.com/sql/default.asp).

