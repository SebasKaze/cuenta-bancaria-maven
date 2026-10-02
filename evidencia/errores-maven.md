# Errores de Maven que encontré

| Queja | La línea clave que dijo Maven | La causa | Cómo lo arreglé |
|---|---|---|---|
| 1 |[FATAL] Non-parseable POM /home/sebastian/cuenta-bancaria-maven/pom.xml: end tag name </dependencia> must match start tag name <dependency> from line 24 (position: TEXT seen ...</version>\n        </dependencia>... @28:23)  @ line 28, column 23 | Esta mal escrito "dependency" | Cambiar dependencia -> dependency |
| 2 | [WARNING] maven-shade-plugin has detected that some files are present in two or more JARs. | Hay un overlapping de clases| Se puede ignorar, no genera un conflicto de momento|
| 3 | [ERROR] 	Could not find artifact com.fasterxml.jackson.core:jackson-databind:jar:2.22.30 in central (https://repo.maven.apache.org/maven2) | No se encuentra la dependencia ya que esta mal escrita| Quitar el 0 la version com.fasterxml.jackson.core:jackson-databind:jar:2.22.30|
| 4 | [ERROR] /home/sebastian/cuenta-bancaria-maven/src/main/java/com/academia/banco/EstadoDeCuenta.java:[16,37] cannot find symbol
  symbol:   class JsonProcessingException
  location: class com.academia.banco.EstadoDeCuenta | No se encuentra la libreria para los Jsons| Cambiar el scope de lugar|
| 5 | Error: no se ha encontrado o cargado la clase principal com.academia.banco.Aplicacion
Causado por: java.lang.ClassNotFoundException: com.academia.banco.Aplicacion
| Esta mal escrito la referencia a App | Cambiar Aplicacion por App|