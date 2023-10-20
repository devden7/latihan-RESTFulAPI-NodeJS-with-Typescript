# Account API Spec

## Register API

Endpoint : POST /account/register

Request Body :

```json
{
  "nama": "test",
  "email": "test@test.com",
  "password": "12345678",
  "repeatPassword": "12345678"
}
```

Response Body :

```json
{
  "message": "Akun Berhasil Dibuat"
}
```

Response Body Error (Email Sudah Digunakan) :

```json
{
  "message": "Email sudah digunakan, silahkan masukan email lain"
}
```

Response Body Error (Email tidak valid) :

```json
{
  "message": "Email tidak valid"
}
```

Response Body Error (Password tidak valid) :

```json
{
  "message": "Password minimal 6 huruf"
}
```

## Login API

Endpoint : POST /account/login

Request body :

```json
{
  "email": "test@test.com",
  "password": "123456"
}
```

Response Body :

```json
{
  "data": {
    "email": "test@test.com",
    "nama": "test",
    "token": "random string from JWT"
  },
  "message": "Login Sukses"
}
```

Response Body Error (Email atau password tidak valid) :

```json
{
  "message": "Email Atau Password Salah"
}
```

## Update Account API

Endpoint : PUT /account/updateAccount

Headers :

- Authorization : token

Request Body :

```json
{
  "data": {
    "email": "test@test.com",
    "newPassword": "87654321",
    "repeatNewPassword": "87654321"
  },
  "message": "Password berhasil diganti"
}
```

Response Body Error (Password tidak valid) :

```json
{
  "data": {
    "message": "Password minimal 6 huruf"
  }
}
```
