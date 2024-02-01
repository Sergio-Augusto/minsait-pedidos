# WebApi (.Net6) and Angular CRUD 

The following project contains: 

## Backend
Tradução - Uma API <b>Backend</b> (lado do servidor) .Net 6.0 com endpoints para CRUD:

O Backend foi desenvolvido de acordo com a especificação Microsoft de <b>D</b>esign <b>D</b>irigido por <b>D</b>omínio (DDD). Existem três projetos-bibliotecas: API / Domínio / Infraestrutura, dentro da pasta UserBackend, cada um com a responsabilidade correspondente ao modelo.
A camada de aplicação (API): ou a camada de apresentação contém todos os endpoints da API e contratos com o cliente.
A camada de Domínio (Domínio): Contém toda a lógica de negócios e validações, sendo responsável por agregar os dados e conter as regras de negócios.
A camada de Infraestrutura: Responsável pela persistência de dados, contendo a implementação do EFC (Entity Framework Core), que suporta diferentes bancos de dados como SQL ou NoSQL.
A API depende do Domínio e da Infraestrutura, a Infraestrutura depende do Domínio, e o Domínio não depende de nenhum outro.
O armazenamento de dados usado para a demonstração foi o banco de dados In-memory da Microsoft, para não criar um serviço adicional para o projeto de demonstração. Ele utiliza os mesmos métodos que o mapeamento normal do banco de dados, usando o EFC.
A validação dos campos do backend foi realizada usando a sintaxe de validação fluente.
## Frontend
Uma aplicação de exemplo CRUD <b>Frontend</b> (lado do cliente) Angular:

O Frontend contém uma grade Angular Material (Visão geral da grade) que, ao mesmo tempo, contém componentes de tabela e componentes de diálogo filhos para exibir os dados da API.
As validações do Frontend foram feitas usando a sintaxe de validação fluente.
As cores da interface do usuário e o design foram selecionados a partir do estilo de design padrão do Angular Material (CSS).
Outros
Um arquivo <b>Docker Compose</b> para orquestrar ambos os serviços com um único comando, cada serviço contém um Dockerfile com a configuração para iniciar o serviço.
Este repositório contém 2 branches, um para desenvolvimento e outro para lançamento.
Para iniciar com o Docker:
docker compose up

Frontend - URL: http://localhost:4200
Para iniciar sem o Docker:
Dentro da pasta /Frontend/ ng serve
Dentro da pasta /Backend/UserBackend/API dotnet run
Endpoints da API
<b>Swagger</b>: https://localhost:7066/swagger/index.html


Utilizar um serviço de banco de dados real e orquestrá-lo com o Docker.
Adicionar testes unitários para todos os serviços.
Adicionar uma etapa de teste Docker para ambos os serviços.
Adicionar rotas e mais visualizações à interface do usuário.
Adicionar suporte SSL.
Histórico de código Git mais limpo no ramo de desenvolvimento.
Adicionar autenticação de usuário.
Adicionar um servidor HTTP como o NGINX para o Frontend Angular.
Adicionar o repositório a um pipeline de CD/CI.
Esta é uma compilação de desenvolvimento e não é recomendada para um ambiente de produção.