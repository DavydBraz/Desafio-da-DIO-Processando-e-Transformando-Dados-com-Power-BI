# Desafio-da-DIO-Processando-e-Transformando-Dados-com-Power-BI
Desafio da DIO Processando e Transformando Dados com Power BI referente ao curso de Python Data Analytics.

##1. Verifique os cabeçalhos e tipos de dados <h2>
Verificando todos os cabeçalhos e tipos de dados estavam corretos, não sendo necessário nenhuma modificação.

##2. Modifique os valores monetários para o tipo double preciso <h2>
Salario estava como double, decimal.

##3. Verifique a existência dos nulos e analise a remoção <h2>
Com base nas verificações só existia uma tabela com valor null, que era referente ao chefe do funcionario, visto a possibilidade do mesmo não ter um chefe, preferi deixar essa informação.

##4. Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente <h2>
Existia apenas 1 funcionario sem chefe.

##5. Verifique se há algum departamento sem gerente <h2>
Não há.

##6.Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas <h2>
Não foi necessário.

##7. Verifique o número de horas dos projetos <h2>
Todos possuiam as horas dos projetos, tendo uma media de: 4 horas, para verificação disso utilizou-se da verificação pelo power bi para confirmação da existência ou não de nulls, e da utilização da consulta sql: SELECT AVG(dnum) FROM project;.

##8. Separar colunas complexas <h2>
Dividi o address pelo delimitador '-', no power bi, ficando em 5 partes, após isso, realizei ajustes para que Fire Oak ficasse junto, e ajustei as colunas desse endereço, para que depois removesse uma dessa colunas que tava só com 1 TX porque esse da rua tinha sido devidido em 2, com esse ajuste passou a ficar certo.

##9. Mesclar consultas employee e departament para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção <h2>
Mesclei como nova consulta atravé do power bi, chamando a nova tabela de Employee_Department, utilizando as colunas de superssn do employee e a mgrssn do department, utilizando o tipo de mescla interna.

##10. Neste processo elimine as colunas desnecessárias <h2>
Não precisei eliminar, aé porque como não foi referenciado o que seria preciso para criar as tabelas, no caso faltando as perguntas de pesquisa, acriditei que seria melhor manter.

##11. Realize a junção dos colaboradores e respectivos nomes dos gerentes . Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo <h2>
Mesclei os colaboradores com os nomes dos gerentes pelo Power BI, criando uma nova tabela chamada Employee_Manager, para isso, utilizei do supersnn do employee mesclando com o ssn do employee, dessa forma sendo possivel extrair o nome dos chefes dos funcionarios, utilizando junção interna. 

##12. Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores <h2>
Mesclei o Nome e sobrenome da coluna de Employee_Manager, utilizando separador ' '.

##13. Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro <h2>
Mesclei departament com dept_locations pelo Power BI, mesclagem interna, utilizando com base do dnumber.

##14. Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir <h2>
Atribuir pode ser útil em certos contextos, porém, a fusão (MERGE) oferece uma abordagem mais robusta e flexível para combinar dados de diferentes fontes e criar relações entre eles em Power BI.

##15. Agrupe os dados a fim de saber quantos colaboradores existem por gerente <h2>
Foi agrupado os colaboradores por gerente em uma outra tabela: Num_Employee_Manager

##16. Elimine as colunas desnecessárias, que não serão usadas no relatório, de cada tabela <h2>
OK

##OBS <h2>
Foi verificado se tinha algum relacionamento faltando, buscando automaticamente, e atribuindo os mesmos. Como não foi solicitado a parte de Dashboard, foi anexado ao documento em questão apenas um visual mais simples, já que faltou o dicionario de dados e não foi possivel a compreensão completa de que era cada dado.
