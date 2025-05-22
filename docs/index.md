# Auth Service

O `auth-service` é responsável por autenticar usuários, registrar contas e gerar tokens JWT. Ele atua como ponto central de segurança na plataforma, delegando o gerenciamento de contas ao `account-service`.

## Funcionalidades:

- **Autenticação**: Permite que usuários façam login utilizando e-mail e senha.
- **Registro de Conta**: Permite que novos usuários se registrem no sistema.
- **Validação de Tokens**: Valida tokens JWT para garantir a autenticidade das requisições.
