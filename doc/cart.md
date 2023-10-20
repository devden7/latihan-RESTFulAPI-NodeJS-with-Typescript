# Cart API Spec

## Add product to Cart

Endpoint : POST /users/add-to-cart

Headers :

- Authorization : token

Request Body :

```json
{
  "product_id": "ObjectId ref dari Product Collection",
  "quantity": 1
}
```

Response Body :

```json
{
  "data": {
    "product_id": "ObjectId ref dari Product Collection",
    "quantity": 1
  },
  "message": "Product berhasil ditambahkan ke cart"
}
```

Response Body Error :

```json
{
  "message": "Gagal menambahkan product ke cart"
}
```

## Get Cart User

Endpont : GET /users/get-cart

Headers :

- Authorization : token

Response Body :

```json
{
  "data": {
    "items": [
      {
        "product_id": "ObjectId ref dari Product Collection",
        "quantity": 1
      },
      {
        "product_id": "ObjectId 2 ref dari Product Collection",
        "quantity": 2
      }
    ]
  },
  "message": "Berhasil mengambil item dari cart"
}
```

Response Body Error :

```json
{
  "message": "gagal memangambil cart"
}
```

## Increase product quantity

Endpoint : PUT /users/increase-cart/:prodId

Headers :

- Authorization

Response Body :

```json
{
  "data": {
      {
        "product_id": "ObjectId ref dari Product Collection",
        "quantity": 3,
      },
  },
  "message": "Berhasil menambah 1 item cart",
}
```

Response Body Error:

```json
{
  "message": "Gagal Menambah item cart"
}
```

## Reduce product quantity

Endpoint : PUT /users/reduce-cart/:prodId

Headers :

- Authorization

Response Body :

```json
{
  "data": {
      {
        "product_id": "ObjectId ref dari Product Collection",
        "quantity": 2,
      },
  },
  "message": "Berhasil mengurangi 1 item cart",
}
```

Response Body Error:

```json
{
  "message": "Gagal mengurangi item cart"
}
```

## Remove cart

Endpoint : DELETE /users/delete-cart/:accountId

Headers :

- Authorization

Response Body :

```json
{
  "message": "Berhasil menghapus semua item dalam cart"
}
```

Response Body Error:

```json
{
  "message": "Gagal menghapus semua item dalam cart"
}
```
