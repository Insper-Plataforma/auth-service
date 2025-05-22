# Endpoints

Base URL: `/auth`

## POST `/auth/register`

Registra um novo usuário.

### Request

```json
{
  "name": "Lucas",
  "email": "lucas@exemplo.com",
  "password": "12345678"
}
```

### Response

```json
{
  "token": "jwt.token.aqui"
}
```

---

## POST `/auth/login`

Autentica e retorna o token.

### Request

```json
{
  "email": "lucas@exemplo.com",
  "password": "12345678"
}
```

### Response

```json
{
  "token": "jwt.token.aqui"
}
```

---

## POST `/auth/solve`

Extrai idAccount do token.

### Request
```json
{
  "token": "jwt.token.aqui"
}
```

### Response

```json
{
  "idAccount": "uuid"
}
```
---