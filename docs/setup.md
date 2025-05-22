# Setup e Dependências - Auth Service

Este microsserviço é responsável pela autenticação da plataforma. Ele integra-se com o `account-service` para criar/validar contas e usa JWT para gerar tokens.

---

## Requisitos

- Java 17+
- Spring Boot
- OpenFeign
- jjwt (Java JWT)
- Lombok

---

## Dependências (pom.xml)

```xml
<dependency>
    <groupId>org.flywaydb</groupId>
    <artifactId>flyway-core</artifactId>
</dependency>
<dependency>
    <groupId>org.postgresql</groupId>
    <artifactId>postgresql</artifactId>
    <scope>runtime</scope>
</dependency>
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
</dependency>
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-validation</artifactId>
</dependency>
<dependency>
    <groupId>io.jsonwebtoken</groupId>
    <artifactId>jjwt</artifactId>
    <version>0.9.1</version>
</dependency>
```

---

## Como compilar

```bash
mvn clean package
```

---
