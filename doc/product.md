# Product API SPect

## Add product

Endpoint : POST /admin/add-product

Headers :

- Authorization : token

Request Body :

```json
{
  "namaProduct": "Product 1",
  "hargaProduct": 1000,
  "urlImageProduct": "https://dummylinkimage.com/",
  "categoryProduct": "Teknologi",
  "stockProduct": 10,
  "DescriptionProduct": "Ini adalah deskripsi Product"
}
```

Response Body :

```json
{
  "data": {
    "id": "ID Random dari MongoDB",
    "namaProduct": "Product 1",
    "hargaProduct": 1000,
    "urlImageProduct": "https://dummylinkimage.com/",
    "categoryProduct": "Technology",
    "stockProduct": 10,
    "DescriptionProduct": "Ini adalah deskripsi Product"
  },
  "message": "Product Berhasil Ditambahkan!"
}
```

Response Body Error (Dari Validation) :

```json
{
  "message": "Nama product minimal 3 huruf"
}
```

## Get product

Endpoint : GET /admin/get-all-products

Response Body :

```json
{
  "data": {},
  "message": "Product berhasil diambil"
}
```

Response Body Error :

```json
{
  "message": "Gagal mengambil product"
}
```

## Update product

Endpoint : PUT /admin/update-product/:prodId

Headers :

- Authorization : token

Request Body :

```json
{
  "namaProduct": "New Product 1", // optional
  "hargaProduct": 10000, // optional
  "urlImageProduct": "https://new-dummylinkimage.com/", // optional
  "categoryProduct": "Technology", // optional
  "stockProduct": 10, // optional
  "DescriptionProduct": "New Ini adalah deskripsi Product" // optional
}
```

Response body :

```json
{
  "data": {
    "id": "ID Random dari MongoDB",
    "namaProduct": "New Product 1", // optional
    "hargaProduct": 10000, // optional
    "urlImageProduct": "https://new-dummylinkimage.com/", // optional
    "categoryProduct": "Technology", // optional
    "stockProduct": 10, // optional
    "DescriptionProduct": "New Ini adalah deskripsi Product" // optional
  },
  "message": "Product Berhasil Diupdate!"
}
```

Response Body Error (Dari Validation) :

```json
{
  "message": "Nama product minimal 3 huruf"
}
```

## Delete product

Endpont : DELETE /admin/delete-product/:prodId

Headers :

- Authorization : token

Response Body :

```json
{
  "message": "Product berhasil dihapus"
}
```

Responses Body Error :

```json
{
  "message": "Product ID tidak ditemukan!"
}
```
