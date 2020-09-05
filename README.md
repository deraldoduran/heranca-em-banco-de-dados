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
```sql
INSERT INTO interior (nome, população, altitude) VALUES 
('QUIXADÁ', 900000, 200), ('QUIXERAMOBIM', 80000, 200), ('SENADOR POMPEU', 20000, 300), 
('BANABUIÚ', 10000, 100), ('ACOPIARA', 40000, 1500), ('PIRIPIRI', 15000, 500), 
('PINDAMONHAGABA', 300000, 1200), ('CANINDÉ', 500000, 300);
```
```sql
CREATE VIEW todas_as_cidades AS SELECT nome, populacao, altitude FROM capitais 
UNION SELECT nome, população, altitude FROM interior
```
```sql
CREATE TABLE IF NOT EXISTS capitais_heranca( 
estado varchar(2) )
INHERITS (interior);
```
```sql
INSERT INTO CAPITAIS_HERANCA (NOME, POPULAçãO, ALTITUDE, ESTADO) VALUES
('FORTALEZA', 500000, 500, 'CE'), ('NATAL', 2000000, 700, 'RN'), 
('SÃO PAULO', 500000, 500, 'SP'), ('RIO DE JANEIRO', 250000, 200, 'RJ');
```
