# ForoHub
El PROYECTO SE ENCUENTRA EN EL ZIP, FAVOR DE DESCARGAR ANTES DE USARLO
API REST para la gestión de tópicos de discusión con autenticación mediante tokens.

## Tecnologías

- Java
- Spring Boot
- MySQL
- JWT
- Spring Security
- JPA

## Funcionalidades

- Autenticación de usuarios mediante token
- Crear tópicos
- Listar tópicos
- Consultar tópico por ID
- Actualizar tópicos
- Eliminar tópicos

## Base de datos

El proyecto utiliza una base de datos relacional con tablas para:

- usuarios
- topicos
- cursos
- respuestas

## Configuración

Crea una base de datos en MySQL:

```sql
CREATE DATABASE forohub;
```

Configura las credenciales en `application.properties` o mediante variables de entorno.

Ejemplo:

```properties
spring.datasource.url=jdbc:mysql://localhost:PUERTO/forohub
spring.datasource.username=USUARIO
spring.datasource.password=CONTRASEÑA
```

También se requiere una clave secreta para el token:

```
JWT_SECRET=tu_clave_secreta
```

## Ejecución

Ejecuta el proyecto con Maven:

```bash
mvn spring-boot:run
```

## Endpoints principales

| Método | Endpoint | Descripción |
|------|------|------|
| POST | `/login` | Autenticación |
| POST | `/topicos` | Crear tópico |
| GET | `/topicos` | Listar tópicos |
| GET | `/topicos/{id}` | Ver tópico |
| PUT | `/topicos/{id}` | Actualizar |
| DELETE | `/topicos/{id}` | Eliminar |
