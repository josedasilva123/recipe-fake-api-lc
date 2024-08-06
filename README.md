Uma fake API para uma aplicação de receitas

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

### Receitas /recipes GET - Leitura múltipla

Padrão de resposta:

```json
[
  {
    "id": 1,
    "title": "Sushi",
    "content": "Integer vitae blandit nulla. Nunc dictum purus a rutrum vehicula. Nullam pulvinar diam iaculis porta euismod. Pellentesque scelerisque turpis lectus, id vulputate tellus mattis eu. Integer sodales volutpat massa eu tempus. Nam faucibus nibh eget ipsum hendrerit laoreet. Nullam tempor in massa in rutrum. Praesent rutrum purus a erat varius efficitur. In laoreet dui lectus, ut sodales urna fermentum in. Vestibulum ut mi imperdiet, hendrerit sapien sit amet, posuere eros. Fusce vitae venenatis sem. Morbi vel dictum mauris. Fusce tempor arcu quis leo tincidunt scelerisque."
  }
]
```

### Receitas /recipes/:id GET - Leitura individual

```json
{
  "id": 1,
  "title": "Sushi",
  "content": "Integer vitae blandit nulla. Nunc dictum purus a rutrum vehicula. Nullam pulvinar diam iaculis porta euismod. Pellentesque scelerisque turpis lectus, id vulputate tellus mattis eu. Integer sodales volutpat massa eu tempus. Nam faucibus nibh eget ipsum hendrerit laoreet. Nullam tempor in massa in rutrum. Praesent rutrum purus a erat varius efficitur. In laoreet dui lectus, ut sodales urna fermentum in. Vestibulum ut mi imperdiet, hendrerit sapien sit amet, posuere eros. Fusce vitae venenatis sem. Morbi vel dictum mauris. Fusce tempor arcu quis leo tincidunt scelerisque."
},
```

### Reviews /reviews POST - Criar review

Padrão de corpo

```json
{
  "grade": 5,
  "recipeId": 1,
  "text": "Integer vitae blandit nulla. Nunc dictum purus a rutrum vehicula."
}
```

Padrão de resposta

```json
{
  "id": 1,
  "grade": 5,
  "recipeId": 1,
  "text": "Integer vitae blandit nulla. Nunc dictum purus a rutrum vehicula."
}
```

### Reviews /reviews GET - Leitura múltipla

Padrão de resposta

```json
[
  {
    "id": 1,
    "grade": 5,
    "recipeId": 1,
    "text": "Integer vitae blandit nulla. Nunc dictum purus a rutrum vehicula."
  }
]
```
