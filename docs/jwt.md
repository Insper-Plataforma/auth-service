# JWT e Segurança

## Criação de Tokens

Feita no `JwtService` usando:

- `issuer`: nome da plataforma (via `.yaml`)
- `secret-key`: chave base64 (via `.yaml`)
- `nbf` e `exp`: início e expiração

---

## Exemplo de Payload

```json
{
  "jti": "idAccount",
  "iss": "auth-service",
  "nbf": 1716673000,
  "exp": 1716759400
}
```

---

## Validação


O `JwtService` valida o token usando:
- `issuer`: nome da plataforma (via `.yaml`)
- `secret-key`: chave base64 (via `.yaml`)
- `nbf` e `exp`: início e expiração
- `jti`: idAccount (campo jti)
- `aud`: público (não utilizado)

Ao resolver o token (solve):

- Verifica se está expirado (exp)
- Verifica se já está ativo (nbf)
- Retorna idAccount (campo jti)

---

## Recomendações

- Armazene o token com segurança
- Use Authorization: Bearer <token>
- Tokens são stateless (não precisam de sessão)

---