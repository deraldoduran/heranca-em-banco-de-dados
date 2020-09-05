# heranca-em-banco-de-dados
```sql
-- Database: heranca_em_BD

CREATE TABLE IF NOT EXISTS capitais(
	nome VARCHAR(30),
	populacao NUMERIC(10,2),
	altitude INT,
	estado CHAR(2)
);
```
```sql
CREATE TABLE IF NOT EXISTS interior(
	nome VARCHAR(30),
	população NUMERIC(10,2),
	altitude int
);
```
