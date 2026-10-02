# Cuenta bancaria — Maven

**Autor:** Hilario Sebastian Espinoza Garcia

## Cómo construir y correr

    ./mvnw clean package
    java -jar target/cuenta-bancaria-maven-1.0.0.jar

## Qué hay en este proyecto

| Qué | Dónde |
|---|---|
| El programa (estado de cuenta en texto y en JSON) | `src/main/java/com/academia/banco/App.java` |
| Las pruebas | `src/test/java/com/academia/banco/` |
| La evidencia de cada mini-práctica | `evidencia/` |
| Los 5 errores de Maven que encontré | `evidencia/errores-maven.md` |

## Boleto de salida

1. ¿Qué diferencia hay entre `./mvnw package` y `./mvnw install`?

Package empaqueta los recursos y el programa y genera un .jar y se guarda en target/. install igualmente empaqueta pero genera una copia local de Maven

2. ¿Por qué `compile` pasó pero `java -jar` falló en la MP-3?

Porque java -jar no descarga las dependencias externas

3. En tu proyecto de Spring Boot, ¿de dónde sale la versión de una dependencia que no tiene 
`<version>`?

Directamente del catalogo de Spring, se heredan las versiones que ya estan probadas

4. ¿Qué va en `settings.xml` y no en `pom.xml`? ¿Por qué?

En pom va todo lo necesario para construir un proyecto. En settings van las configuraciones necesarias como contraseñas o tokens, entre otros. Esos no pueden ir en pom por un tema de seguridad
