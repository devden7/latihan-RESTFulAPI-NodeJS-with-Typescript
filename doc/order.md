# Order API Spec

## Add order from user

Endpont : POST /users/add-order

Headers :

- Authorization : token

Request Body :

```json
{
  "products": [
    {
      "product_id": "ObjectId ref dari id product",
      "quantity": 1,
      "price": 20000
    }
  ],
  "total_price": 20000,
  "order_date": "Date.now()",
  "payment": "Gopay",
  "status_order": "Pending"
}
```

Response Body :

```json
{
  "data": {
    "_id": "ObjectId From mongodb",
    "account_id": "ObjectId ref dari id account",
    "products": [
      {
        "product_id": "ObjectId ref dari id product",
        "quantity": 1,
        "price": 20000
      }
    ],
    "total_price": 20000,
    "order_date": "Date.now()",
    "payment": "Gopay",
    "status_order": "Pending"
  },
  "message": "Order berhasil!"
}
```

Response Body Error :

```json
{
  "message": "Gagal Melakukan Order!"
}
```

## Get user list order

Endpoint : GET /users/get-all-order

Headers:

- Authorization : token

Response Body :

```json
{
  "data": {},
  "message": "Berhasil mengambil list order user"
}
```

Response Body Error :

```json
{
  "message": "Gagal mengambil list order user"
}
```

## Get user list single order

Endpoint : GET /user/:orderId

Headers:

- Authorization : token

Response Body :

```json
{
  "data": {},
  "message": "Berhasil mengambil single order user"
}
```

Response Body Error :

```json
{
  "message": "Gagal mengambil single order user"
}
```

## Get Admin list order

Endpoint : GET /admin/get-admin-all-order

Headers:

- Authorization : token

Response Body :

```json
{
  "data": {},
  "message": "Berhasil mengambil list order admin"
}
```

Response Body Error :

```json
{
  "message": "Gagal mengambil list order admin"
}
```

## Get Admin list single order

Endpoint : GET /admin/:orderId

Headers:

- Authorization : token

Response Body :

```json
{
  "data": {},
  "message": "Berhasil mengambil single order admin"
}
```

Response Body Error :

```json
{
  "message": "Gagal mengambil single order admin"
}
```

## Add order from admin to user

Endpoint : PUT /admin/:prodId

Headers :

- Authorization : token

Request Body :

```json
{
  "status_order": "Dikirim / Dibatalkan"
}
```

Response Body :

```json
{
  "message": "Berhasil Dikirim / Dibatalkan"
}
```

Response Body Error:

```json
{
  "message": "Id order tidak ditemukan"
}
```
