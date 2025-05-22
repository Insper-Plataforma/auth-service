# Arquitetura

## Estrutura do Projeto

```bash
src/main/java/store/auth/
│ ├── AuthApplication.java # Classe principal
│ ├── AuthResource.java # Controller REST
│ ├── AuthService.java # Regras de negócio
│ ├── JwtService.java # Lógica de geração/validação JWT
│ ├── AuthParser.java # Conversão entre DTOs
│ └── Register.java # Entidade local
├── resources/
│ └── application.yaml # Configurações do serviço
```

---

## Comunicação com Account Service

O `AuthService` se comunica diretamente com `account-service` via **Feign Client**, exposto por `AccountController`, para criar e autenticar contas.

- Registro → chama `accountController.create(...)`
- Login → chama `accountController.findByEmailAndPassword(...)`