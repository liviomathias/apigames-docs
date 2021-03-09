# API de Games
Esta API é foi desenvolvida para o estudo de NodeJS e algumas features como autenticação JWT.

## Endpoints

### POST /auth
Esse endpoint é responsável pela autenticação do usuário.
#### Parametros
```
{
    "email": "user@gmail.com",
    "password": 2345678
}
```
#### Respostas
##### OK! 200
Caso essa reposta aconteça, sua aplicação receberá um token de acesso a todas as APIS's do sistema.

Exemplo de resposta: 

```
{
    "token": "99999999999999999999999999999999999999999999999999999"
}

```
##### Falha na autenticação! 401
Caso essa resposta aconteça, pode ter ocorrido alguma falha na requisição ou falha no processo de autenticação. Como e-mail ou senha incorreta.

Exemplo de resposta:

```
{
    "err": "Invalid credentials"
}
```


### GET /games
Esse endpoint retorna a listagem de todos os games cadastrados no banco de dados.
#### Parametros
Nenhum
#### Respostas
##### OK! 200
Caso essa reposta aconteça, você receberá a listagem de todos os games.

Exemplo de resposta: 

```
[
    {
        "id": 1,
        "title": "God of War IV",
        "year": 2018,
        "price": 59
    },
    {
        "id": 2,
        "title": "Red Dead Redemption II",
        "year": 2018,
        "price": 65
    },
    {
        "id": 3,
        "title": "Ghost of Tsushima",
        "year": 2020,
        "price": 80
    },
    {
        "id": 4,
        "title": "Fall Guys",
        "year": 2020,
        "price": 29.9
    },
    {
        "id": 5,
        "title": "Horizon The New Dawn",
        "year": 2017,
        "price": 59
    },
    {
        "id": 6,
        "title": "GTA V Online Edition",
        "year": 2014,
        "price": 45
    }
   
]

```
##### Falha na autenticação! 401
Caso essa resposta aconteça, pode ter ocorrido alguma falha na requisição ou falha no processo de autenticação. Como Token Inválido ou Token expirado.

Exemplo de resposta:

```
{
    "err": "Invalid Token!"
}
```
