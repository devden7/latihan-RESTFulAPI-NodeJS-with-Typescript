# Review API Spec

## Add Review

Endpoint : POST /users/add-review/:prodId

Headers :

- Authorization : token

Request Body :

```json
{
  "rating": "5",
  "comment": "Product ini sangat bagus"
}
```

Response Body :

```json
{
  "message": "Rating berhasil ditambahkan!"
}
```

Response Body Error :

```json
{
  "message": "Gagal menambahkan rating!"
}
```

## Get User Review

Endpoint : GET /users/get-rating-user

Headers :

- Authorization : token

Response Body :

```json
{
  "data": {},
  "message": "Rating user berhasil diambil!"
}
```

Response Body Error :

```json
{
  "data": {},g
  "message": "Rating product gagal diambil!"
}
```

## Get All Review product

Endpoint : GET /users/get-all-review

Response Body :

```json
{
  "data": {},
  "message": "Rating product berhasil diambil!"
}
```

Response Body Error :

```json
{
  "data": {},
  "message": "Rating product gagal diambil!"
}
```
