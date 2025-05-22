# Auth Service

O `auth-service` é responsável por autenticar usuários, registrar contas e gerar tokens JWT. Ele atua como ponto central de segurança na plataforma, delegando o gerenciamento de contas ao `account-service`.

## Funcionalidades:

- Registro de usuários
- Login com email e senha
- Geração de token JWT
- Resolução de token (quem é o usuário?)
- Integração com `account-service` via Feign Client
