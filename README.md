Uma fake API para uma aplicação de notícias

## PARA INICIAR

Para iniciar está API, realize o clone deste repositório e rode os seguintes comandos

_Baixar dependências_

```bash
npm install
/* Necessário somente uma vez, para realizar o download das dependências */
```

_Rodar projeto localmente_

```bash
npm run start
```

## ROTAS

### Notícias /posts GET - Leitura múltipla

Padrão de resposta:

```json
[
  {
    "id": 1,
    "categoryId?": 1,
    "title": "Lorem ipsum dolor sit amet 2",
    "excerpt?": "Integer vitae blandit nulla.",
    "content": "Integer vitae blandit nulla. Nunc dictum purus a rutrum vehicula. Nullam pulvinar diam iaculis porta euismod.",
    "image?": "https://images.pexels.com/photos/1181352/pexels-photo-1181352.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
  }
]
```

#### Parâmetros (Query)

| Parâmetro  | Descrição                                 |
| ---------- | ----------------------------------------- |
| categoryId | Busca os posts conforme o id de categoria |

### Notícias /posts/:id GET - Leitura individual

```json
{
    "id": 1,
    "categoryId?": 1,
    "title": "Lorem ipsum dolor sit amet 2",
    "excerpt?": "Integer vitae blandit nulla.",
    "content": "Integer vitae blandit nulla. Nunc dictum purus a rutrum vehicula. Nullam pulvinar diam iaculis porta euismod.",
    "image?": "https://images.pexels.com/photos/1181352/pexels-photo-1181352.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
  },
```

### Categorias /categories GET - Leitura múltipla

Padrão de resposta:

```json
[
  {
    "id": 1,
    "slug": "economia",
    "label": "Economia"
  },
  {
    "id": 2,
    "slug": "seguranca",
    "label": "Segurança"
  },
  {
    "id": 3,
    "slug": "mundo",
    "label": "Mundo"
  }
]
```

### Comentários /comments POST - Criar comentário

Padrão de corpo

```json
{
  "postId": 1,
  "author": "Osvaldo",
  "text": "Integer vitae blandit nulla. Nunc dictum purus a rutrum vehicula."
}
```

Padrão de resposta

```json
{
  "id": 1,
  "postId": 1,
  "author": "Osvaldo",
  "text": "Integer vitae blandit nulla. Nunc dictum purus a rutrum vehicula."
}
```

### Comentários /comments GET - Leitura múltipla

Padrão de resposta

```json
[
  {
    "id": 1,
    "postId": 1,
    "author": "Osvaldo",
    "text": "Integer vitae blandit nulla. Nunc dictum purus a rutrum vehicula."
  }
]
```
