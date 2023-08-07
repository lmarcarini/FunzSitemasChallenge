# Desafio

Olá desenvolvedor, pronto para participar do nosso processo de seleção para a nossa vaga de pessoa desenvolvedora backend?

## Instruções

Crie uma aplicação que exponha uma API RESTful de criação de usuários e login.
Todos os endpoints devem aceitar e responder somente JSON, inclusive ao responder mensagens de erro.

### Cadastro

- Esse endpoint deverá receber um usuário com os campos "nome", "email", "senha", mais uma lista de objetos "endereço", seguindo o formato abaixo:

```json
    {
        "name": "José Soares",
        "email": "jose@soares.com",
        "password": "secret",
        "address": [
            {
                "street": "rua abc",
                "number": "210",
                "distric": "centro",
                "city": "Belo Horizonte",
                "state": "MG",
                "country": "Brasil"
            }
        ]
    }
```

- Responder o código de status HTTP apropriado
- Em caso de sucesso, retorne o usuário com seguintes campos:
    - `id`: id do usuário (pode ser o próprio gerado pelo banco, porém seria interessante se fosse um GUID)
    - `created`: data da criação do usuário
    - `modified`: data da última atualização do usuário
    - `last_login`: data do último login (no caso da criação, será a mesma que a criação)
    - `token`: token de acesso da API (pode ser um GUID ou um JWT)

- Caso o e-mail já exista, deverá retornar erro com a mensagem "E-mail já existente".
- O token deverá ser persistido junto com o usuário

### Login

- Este endpoint irá receber um objeto com e-mail e senha.
- Caso o e-mail e a senha correspondam a um usuário existente, retornar igual ao endpoint de Criação.
- Caso o e-mail não exista, retornar erro com status apropriado mais a mensagem "Usuário e/ou senha inválidos"
- Caso o e-mail exista mas a senha não bata, retornar o status apropriado mais a mensagem "Usuário e/ou senha inválidos"

### Perfil do Usuário
- Caso o token não exista, retornar erro com status apropriado com a mensagem "Não autorizado".
- Caso o token exista, buscar o usuário pelo `id` passado no path e comparar se o token no modelo é igual ao token passado no header.
- Caso não seja o mesmo token, retornar erro com status apropriado e mensagem "Não autorizado"
- Caso tudo esteja ok, retornar o usuário no mesmo formato do retorno do Login.

## Avaliação

O que vamos avaliar:

- Desempenho;
- Manutenibilidade;
- Organização;
- Boas práticas.

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


## Requisitos desejáveis
- JWT como token
- Testes unitários
