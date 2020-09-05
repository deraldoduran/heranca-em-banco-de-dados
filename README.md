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
```sql
INSERT INTO capitais (NOME, POPULACAO, ALTITUDE, ESTADO) VALUES
('FORTALEZA', 500000, 500, 'CE'), ('NATAL', 2000000, 700, 'RN'),
('SÃO PAULO', 500000, 500, 'SP'), ('RIO DE JANEIRO', 250000, 200, 'RJ');
```
