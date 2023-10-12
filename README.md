# PowerBI_DIO_Projeto2

Projeto Power BI Com conexão ao banco de dados externo

Git HUB [Geral]: 
https://github.com/julianazanelatto/power_bi_analyst/tree/main/Módulo%203/Desafio%20de%20Projeto


1-> Criando uma instância no postgreeSQL online:
https://customer.elephantsql.com/instance


Git HUB [crate table]: 
https://github.com/julianazanelatto/power_bi_analyst/blob/main/Módulo%203/Desafio%20de%20Projeto/script_bd_company.sql

2-> Criado as tabelas:
Employee, dependent, departament, dept_locations, project, works_on


Git HUB [insert data]: 
https://github.com/julianazanelatto/power_bi_analyst/blob/main/Módulo%203/Desafio%20de%20Projeto/insercao_de_dados_e_queries_sql.sql

3-> Realizado inserta nas tabelas:
Employee, dependent, departament, dept_locations, project, works_on

4-> Realizar a conexão do Postgree com o PowerBI

5-> Importando a tabelas e realizando os ajustes:

5.1 Verificado importação dos cabeçalhos 
	- não houve a necessidade de ajuste
5.2 ajustando os valores monetários
	- não houve a necessidade de ajuste
5.3 Verificando a existência de valores nulos e análise de remoção
	- não houve a necessidade de ajuste
5.4 Verificado na tabela (public employees) se existe alguém sem gerente - campo super_ssn (se estiver nulo, pode não ter gerente)
	- não houve a necessidade de ajuste
5.5 Verificado na tabela (public departament) se existe algum sem gerente
	- não houve a necessidade de ajuste
5.6 verificado o número de horas do projeto na tabela (public project / public works_on)
	- não houve a necessidade de ajuste
5.7 mesclado as tabela (public employee e public departament)
	- Realizado a mescla utilizando os campos chaves (public employee.super_ssn e public departament.mgr_ssn)
	- Criado uma nova tabela employee_depart
5.8 - realizado a junção do nome e sobrenome do employee.
	- Criado uma nova coluna utilizando a formula DAX concatenate 
	Nome = CONCATENATE('public employee'[fname], CONCATENATE(" ", 'public employee'[lname]))
6-> Criado visões de análise de base de dados
![image](https://github.com/alexsansantos/PowerBI_DIO_Projeto2/assets/142915856/e7b6972a-2354-47dc-bdf0-5cf3580c9295)
