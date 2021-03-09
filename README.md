# API de Games
Esta API é foi desenvolvida para o estudo de NodeJS e algumas features como autenticação JWT.

## Endpoints
### GET /games
Esse endpoint retorna a listagem de todos os games cadastrados no banco de dados.
#### Parametros
Nenhum
#### Respostas
##### OK! 200
Caso essa reposta aconteça, você receberá a listagem de todos os games
##### Falha na autenticação! 401
Caso essa resposta aconteça, pode ter ocorrido alguma falha na requisição ou falha no processo de autenticação. Como Token Inválido ou Token expirado.

