#API do INSTAGRAM

## Tecnologias
-NodeJS
-ExpressJS
-MySQL

### Recursos
-Usuarios
-Post
-Comentarios
-Curtidas

### Estrutura do Dados

https://mermaid.live


```mermaid
classDiagram
    Usuario --> Post: OneToMany
    Usuario --> Comentario: OneToMany
    Post --> Comentario: OneToMany
    Post --> Curtida:OneToMany
    Usuario --> Curtida: OneToMany
    class Usuario{
        +id
        +nome
        +nickname
        +bio
        +foto
        +email
        +senha
        +criado_em
        +atualizado_em
    }
    class Post{
        +id
        +usuario_id
        +foto
        +legenda
        +localizacao?
        +criado_em
        +atualizado_em?
    }
    class Comentario{
        +id
        +usuario_id
        +post_id
        +conteudo
        +criado_em

    }
    class Curtida{
        +id
        +usuario_id
        +post_id
        +criado_em
    }


```