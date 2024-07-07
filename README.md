# 💡CaseAccenture - Isabelle Nunes Ferreira

## 🖥️ Sobre o projeto
* O banco de dados utilizado para a crição das tabelas foi *SQL SERVER*
* A linguagem utilizada para criação da API do Backend foi *C#*
* A linguagem utilizada para criação da tela do Frontend foi *VUE.JS e HTML*

- Foi necessária a instalação das seguintes ferrementas:
  * [Visual Studio](https://visualstudio.microsoft.com/pt-br/downloads/)
  * [SSMS - SQL SERVER MANAGEMENT STUDIO](https://learn.microsoft.com/pt-br/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16)
  * [SQL SERVER](https://www.microsoft.com/pt-br/sql-server/sql-server-downloads)

## 📌 Informações sobre o desenvolvimento do case e imagens da aplicação

### 🎛️ Banco de dados✨
- Para a criação das entidades bases necessárias e suas propriedades, foi necessária a utilização do *SQL Server*.
  * Após a criação do login do SSMS, iniciou-se a análise em relação ás colunas e relacionamentos que deveriam existir para atender a lógica solicitada.

- Para a tabela de Empresas foi seguida a estrutura sugerida e a lógica de que os campos de CNPJ, CEP e NomeFantasia são obrigatórios para cadastro.
  
- Para a tabela de Fornecedores foi seguida a lógica da não obrigatoriedade do preenchimento dos campos de CNPJ, CPF, RG e Data de Nascimento, por haver a possibilidade de ser pessoa juridica, e determinados campos serem aceitos vazios.
  * Os campos de CNPJ e CPF estão como opcionais para que o usuário possa fazer a escolha de preenchimento, sendo necessário pelo menos uma delas ser preenchida. A verificação em relação a esta regra está sob responsabilidade da API durante a requisição de POST.

- Por haver a vinculação entre as tabelas de *Empresas e Fornecedores*, foi necessária a criação de uma 3ª tabela, a *RelEmpresaFornecedores*, para armazenar este relacionamento tendo como chaves estrangeiras os IDs das tabelas anteriormente citadas.
  
![image](https://github.com/IsabelleNFerreira/CaseAccenture/assets/71455630/054100c7-a69b-4a8f-912a-e2512046a6ca)

### ☎️ API do Back-end✨
- Para o Backend, utilizando a liguagem C#, foi desenvolvida a API para realizar as requisições necessárias quando conectada ao banco de dados utilizado anteriormente.
  
- É possivel visualizá-la e testá-la diretamente pelo Swagger que é gerado no navegador ao rodar o arquivo.
  
- Na imagem abaixo é possivel visualizar os endpoints de CRUD desenvolvidos de acordo com seu agrupamento de Empresa, Fornecedor, e RelEmpresaFornecedores.
  
![image](https://github.com/IsabelleNFerreira/CaseAccenture/assets/71455630/a5bfddb0-aea5-48aa-a6d6-3c2efd39d9e0)

### 🔗 Tela do Front-end✨
- Na tela desenvolvida é possivel visualizar os dados existentes no banco de dados nas tabelas de Empresas, Fornecedores e Vinculos ja cadastradas, todos com os botões de EDIÇÃO e DELEÇÃO.

- Por Empresas ter campos simples, acima da tabela estão presentes os espaços para serem preenchidos na inserção, seguido do botão para esta realização.
  
- Na tabela de Fornecedores, é seguida a estrutura de tabela para visualização, porém pela necessidade de validações em relação aos documentos e data de nascimento, seria de melhor manuseio por parte de usuários, o preenchimento em uma tela ou popup dedicada a este fim.
  
- A tabela de Empresas e Fornecedores a estrutura é semelhante, e nela também existe um botão para direcionar para uma tela de vinculação a ser implementada.
  * Nela seria possivel escolher as empresas ja criadas e fazer o vinculo com fornecedores, e realizar as verificações adequadas de forma mais agradável.

![image](https://github.com/IsabelleNFerreira/CaseAccenture/assets/71455630/2d6a584e-830f-411f-9296-7c31aa059325)



