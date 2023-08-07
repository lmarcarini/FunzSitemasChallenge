# Desafio

    A startup “Seu Direito” tem uma ideia de negócio muito interessante para o setor jurídico e precisa implementar um protótipo desta ideia. 
    O projeto consiste em um sistema que permitirá a contratação de serviços jurídicos, tendo como principais atores 
    da plataforma os “Advogados” e às “Empresas” que necessitam de algum serviço prestado pelo advogado.

## As funcionalidades a serem implementadas são:

- Cadastro de Advogados que deverá conter:
    Nome, telefone, e-mail e CPF.

- Cadastro de Empresas que deverá conter:
    Nome da empresa e ramo de atuação

- Cadastro de Ordens de Serviço Jurídico que deverá conter:
    empresa que está solicitando o serviço, título, descrição, onde será informado o motivo pela qual a empresa precisa de um advogado (Ex: Empresa X está sendo processada pelos seus clientes.)
    
## Regras
- Somente empresas podem criar Ordens de Serviço
- Status da ordem de serviço que poderão ser:
    - Criada – Status inicial quando a empresa cria uma ordem de serviço
    - Delegada – Quando a empresa define qual advogado irá executar o serviço
    - Finalizada – Quando a empresa confirma que o advogado executou o serviço com sucesso
- Os advogados deverão ter a possibilidade de visualizar as Ordens de serviço criada pelas empresas e informar os valores que desejam receber para executar a ordem de serviço
- A Empresa deve visualizar as propostas dos advogados e definir qual a proposta será aceita. Ao fazer este processo o status da ordem deverá ficar como “Delegada”.

## Stack
Para o desafio você deverá utilizar Node + Typescript.


## Requisitos
- Banco de dados em memória, de preferência SQLite.
- Gestão de dependências via Yarn.
- Persistência com ferramenta de ORM adequada.
- Escolha livre de framework.
- Prazo de 3 dias corridos.
- Entregar um repositório público (github) com o código fonte.
- Entregar a API rodando em algum host (Heroku, AWS, etc).
- Utilização de um formatador de código (ex.: prettier) e um lint (ex.: lint) integrados ao projeto
- Crie um **PROJECT.md** com a explicação de como devemos executar o projeto.

## O que iremos Avaliar?

- Organização do código
- Organização no controle de versão
- Complexidade, modularização e acoplamento de código
- Usabilidade da aplicação
- Documentação com orientações para execução do desafio

## Será um diferencial:

- Entregar testes unitários
- Utilizar ferramentas de automação de ambientes e deploy (Ex: Docker)

## Informações para entrega do desafio:
- O teste será analisado e avaliado de acordo com o esforço que foi aplicado ao desafio. Para entregar o desafio você deverá enviar o link do repositório e as instruções para acesso ao sistema.
