Passo 1: Criando uma Tabela no HackMD.io

HackMD.io é um editor de markdown colaborativo que permite criar tabelas usando a sintaxe markdown. Para criar uma tabela, siga estas etapas:

Abra o HackMD.io e crie um novo documento ou abra um existente.


Por exemplo: 
| ID | Nome | Idade |
|----|------|-------|
| 1  | João | 25    |
|----|------|-------|
| 2  | Ana  | 30    |
![image](https://github.com/user-attachments/assets/a260e9fb-d3a8-4002-93f4-64f54bc56f93)

Passo 2: Exportando a Tabela do HackMD.io

Para exportar a tabela do HackMD.io, siga estas etapas:

Clique nos três pontos no canto superior direito do documento.
Selecione "Exportar" no menu suspenso.
Escolha "CSV" como o formato de exportação.
Clique em "Exportar" para baixar o arquivo CSV.
Passo 3: Importando a Tabela para o MySQL

Para importar a tabela para o MySQL, siga estas etapas:

Abra o seu cliente MySQL (por exemplo, phpMyAdmin, MySQL Workbench ou a ferramenta de linha de comando).
Crie um novo banco de dados ou selecione um existente.
Crie uma nova tabela com os mesmos nomes de coluna da sua tabela HackMD.io:
sql
 |
 |
 v

CREATE TABLE minha_tabela (
  ID INT,
  Nome VARCHAR(255),
  Idade INT
); 
LOAD DATA INFILE 'caminho/para/seu/arquivo.csv' INTO TABLE minha_tabela FIELDS TERMINATED BY ',' ENCLOSED BY '\"' LINES TERMINATED BY '\n';



Substitua "caminho/para/seu/arquivo.csv" pelo caminho real do seu arquivo CSV.

Pronto! Você criou com sucesso uma tabela no HackMD.io e a importou para o MySQL.
