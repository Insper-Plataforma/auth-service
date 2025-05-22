# Componentes Internos

## AuthService

- Contém a lógica de registro, login e verificação de tokens.
- Utiliza o `AccountController` para delegar ações de conta.
- Gera tokens com `JwtService`.

---

## JwtService

- Cria tokens JWT com `idAccount`, `nbf` (not before) e `exp` (expiration).
- Valida tokens recebidos e extrai o `idAccount`.
- Usa `jjwt` (Java JWT) com chave secreta vinda do `application.yaml`.

---

## AuthResource

- Expõe os endpoints REST definidos pela interface `AuthController`.
- Encapsula chamadas ao serviço e responde com DTOs (`TokenOut`, `SolveOut`).

---

## AuthParser

- Converte `RegisterIn` → `Register`
- Converte `String` → `TokenOut`

---

## Register (entidade local)

Representa os dados de um registro (nome, email, senha).
