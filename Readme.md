Esse é um repositório de estudo.

Por aqui estou armazenando as informações do Deploy de uma aplicação desenvolvida pela KodeKloud que permite a votação entre gato ou cachorro e permite ver tbm a contagem de votos.

A aplicação toda consiste nos seguintes serviços

## Arquitetura

### FrontEnd
- Vote app (Python)
- Result app (Node.js)
* Acessados pelo usuário externo

### Cache
- Redis (Serve para armazenar temporariamente os votos)
* Acessado pelo VoteApp e pelo Worker

### Bando de dados
- Postgresql (Armazenamento persistente para os votos)
* Acessado pelo ResultApp e pelo Worker

### Integração
- Worker app (.Net - Serve para fazer a integração dos votos enviados ao Redis com o banco de dados para persistência de dados)