# Auth Service

O `auth-service` é responsável por autenticar usuários, registrar contas e gerar tokens JWT. Ele atua como ponto central de segurança na plataforma, delegando o gerenciamento de contas ao `account-service`.

---

## Funcionalidades:

- **Autenticação**: Permite que usuários façam login utilizando e-mail e senha.
- **Registro de Conta**: Permite que novos usuários se registrem no sistema.
- **Validação de Tokens**: Valida tokens JWT para garantir a autenticidade das requisições.

---

## Integração com Jenkins

Este projeto conta com um arquivo Jenkinsfile (na raiz do repositório) que define uma pipeline de integração contínua para compilar automaticamente o módulo sempre que houver alterações no repositório.

### Para que serve?

- Compilação automatizada: toda alteração no repositório dispara o build do Maven, detectando problemas de compilação antes do merge.

- Imagens Docker consistentes: gera e publica automaticamente imagens multiplataforma, facilitando o deploy em diferentes ambientes (x86_64 e ARM).

- Segurança das credenciais: utiliza credenciais armazenadas no Jenkins (identificador dockerhub-credential), evitando exposição de senhas no código.

Dessa forma, a integração com Jenkins garante que o auth-service esteja sempre compilando e empacotado corretamente, com uma imagem Docker pronta para ser implantada nos clusters de produção ou QA.
