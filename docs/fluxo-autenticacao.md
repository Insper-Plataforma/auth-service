# Fluxo de Autenticação

## 1. **Usuário se registra**

   - Envia nome, email, senha
   - `auth-service` chama `account-service` para criar a conta
   - Um token JWT é gerado e retornado

## 2. **Usuário faz login**

   - Envia email e senha
   - `auth-service` autentica via `account-service`
   - Um novo token JWT é gerado e retornado

## 3. **Token é resolvido**

   - Serviços internos usam `/auth/solve` para extrair `idAccount`
