## MySQL

## criar um banco
CREATE DATABASE <br/>

CREATE = CRIAR <br/>

## remover um banco
DROP DATABASE <br/>

DROP = DELETAR <br/>

## TIPOS DE DADOS 

texto = VARCHAR(1000) (X) <br/>
numero = INT (x) <br/>
datas = TIMESTEMP; DATE;

           
## Recursos CRUD 

sempre utileze o WHERE

## C = create ( criar dados ) = INSERT INTO 
## R = read ( ler dados ) = SELECT (WHERE)
## U = update ( carregar dados ) = UPDATE
## D = delete ( deletar dados ) = DELETE

## EXEMPLOS 
INSERT INTO (); <br/>
VALUES ();

## COMO INDETIFICAR UM DADO 
 WHERE
SELECT * FROM celulares <br/>
WHERE garantia > 30 dias;
ou
WHERE nome = "iphone XR"



## UPDATE   
trava do MySQL Workbanch ## SET SQL_SAFE_UPDATES =0;

INSERT INTO celulares (...) <br/>
VALUES ( );
  
UPDATE celulares SET bateria = "100 WHERE iphones = "iphone_XR"; <br/>
a coluna que voce quer editar 

## DELETE 

DELETE * FROM celulares WHERE iphone = "iphone_XR"; 


## CONSTRAINTS

CREATE TABLE celulares (
  id INT PRIMARY KEY AUTO_INCREMENT NOT NULL, <br/>
  aparelhos VARCHAR(100), <br/>
  gigas INT, <br/>
  bateria INT, <br/>
  garantia DATE <br/>
   );

## CONSTRAINTS - relação - FOREIGN KEY 

CREATE TABLE iphones_vitrine (
  id INT PRIMARY KEY AUTO_INCREMENT NOT NULL, <br/>
  fornecedor VARCHAR(200), <br/>
  garantia VARCHAR(100), <br/>
  iphones_vitrine_id INT NOT NULL, <br/>
  FOREING KEY (iphones_vitrine_id) REFERENCES iphones_vitrine(id),
  
  );
INSERT INTO iphones_vitrine(iphone, gigas, bateria, garantia) <br/>
VALUE ();


        
## ALTERAR UMA TABELA 

ALTER TABLE (nome da tabela) ADD COLUMN (nome da coluna que voce vai adicionar) VARCHAR (300); <br/>
ALTER TABLE (nome da tabela) DROP COLUMN (nome da coluna que voce vai remover); 

## SELECIONAR TODOS OS DADOS DE UMA TABELA
SELECT * FROM (nome da tabela);


## JOIN 

INNER JOIN  <br/>
LEFT JOIN  <br/>
RIGHT JOIN <br/>

SELECT celulares.nome, iphones_vitrine.*
FROM celulares
JOIN iphones_vitrine ON celulares.id = iphones_vitrine.celulares_id;

## CMD IMPORTANTES 

- COUNT(): conta o número de linhas em uma tabela ou consulta. 
- SUM(): calcula a soma de valores em uma coluna específica.
- AVG(): calcula a média de valores em uma coluna específica.
- MIN(): encontra o valor mínimo em uma coluna específica.
- MAX(): encontra o valor máximo em uma coluna específica.
- CONCAT(): concatena duas ou mais cadeias de caracteres juntas.
- LENGTH(): retorna o comprimento de uma cadeia de caracteres.
- SUBSTRING(): retorna uma parte de uma cadeia de caracteres.
- UPPER(): converte uma cadeia de caracteres para maiúsculas.
- LOWER(): converte uma cadeia de caracteres para minúsculas.
- NOW(): retorna a data e hora atuais.
- CURDATE(): retorna a data atual.
- CURTIME(): retorna a hora atual.
 
 ## EXEMPLOS

SELECT COUNT(*) FROM clientes; <br/>
SELECT SUM(valor_compra) FROM vendas; <br/>
SELECT UPPER(nome) FROM clientes; 














