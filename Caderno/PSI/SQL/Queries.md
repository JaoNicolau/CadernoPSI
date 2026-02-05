
Select - Selecionar dados
Count - Contar linhas
AVG - fazer a média
SUM - somar 
MAX - Encontrar o máximo
MIN - Encontrar omínimo
WHERE - Encontrar algo "Onde" alguma coisa
GROUP BY - agrupa linhas com os mesmos valores
order by - ordena do menor para o maior (por default) depois se colocar: 
	ASC - fica ascendente 
	DESC - descendente


==Exemplos de queries:==

==Selecionar todos os IDs da tabela my_table==

SELECT id
    FROM my_table;

  
==Seleionar todas as linhas com todos os atributos da tabela my_table==

SELECT *
    FROM my_table;

  
==Contar o número total de registos na tabela my_table==

SELECT COUNT(*) AS total_registos
    FROM my_table;


==1. Contar o numero de colaboradores da empresa com alias "total_employees"==

SELECT COUNT(*) AS total_employees
    FROM my_table;

  
==2. Somar os salarios de todos os colaboradores com alias "total_salaries"==--

SELECT SUM(salary) AS total_salaries
    FROM my_table;

  
==3. Calcular a media das idades dos colaboradores com alias "average_age

SELECT AVG(age) AS average_age
    FROM my_table;

  
==4. Calcular a media dos salarios dos colaboradores com alias "average_salary

SELECT AVG(salary) AS average_salary
    FROM my_table;


==5. Encontrar o salario mais alto dos colaboradores com alias "max_salary

SELECT MAX(salary) AS max_salary
    FROM my_table;

  
==6. Encontrar o salario mais baixo dos colaboradores com alias "min_salary

SELECT MIN(salary) AS min_salary
    FROM my_table;

  
==7. Encontrar o numero de colaboradores com idade superior a 30 anos com alias== =="employees_above_30"==

SELECT * AS employees_above_30
    FROM my_table
    WHERE age > 30;

  
==8. Listar os nomes dos colaboradores do departamento de Marketing==

SELECT id, name
    FROM my_table
    WHERE department = 'marketing';
    

==9. Calcular o numero de colaboradores em cada departamento==

SELECT department, COUNT(id)
    FROM my_table
    GROUP BY department;
    

==10. Calcular o numero de colaboradores em cada idade==

SELECT age, COUNT(id)
    FROM my_table
    GROUP BY age
    ORDER BY age;


==11. Soma dos salarios por departamento==

SELECT department, SUM(salary) AS total_salary
    FROM my_table
    GROUP BY department;


==12. Media das idades por departamento==

SELECT department, AVG(age) AS average_age
    FROM my_table
    GROUP BY department
    ORDER BY department;


==13. Numero de colaboradores com salario superior a 52000==

SELECT COUNT(id) AS employees_above_52000
    FROM my_table
    WHERE salary > 52000;


==14. Encontrar o colaborador com o id = 1==

SELECT *
    FROM my_table
    WHERE id = 1;


