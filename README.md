#  Reto de Automatización QA – Backend  

Este proyecto contiene **suite de pruebas automatizadas** de APIs, para la API de Usuarios de [ServeRest]
(https://serverest.dev/) utilizando **Karate DSL**

## Contenido del proyecto

- `src/test/java/resources/features/GestionUsuarios` : Archivos `.feature` con los escenarios de prueba / CRUD Usuarios.  
- `src/test/java/resources/features/Sesion` : Archivos `.feature` con los escenarios de prueba / Login.  
- `src/test/java/karate/runner/TestRunner.java` : Clase para ejecutar pruebas en paralelo.  
- `src/test/java/resources/response/` : Archivos JSON de schemas para validar respuestas.  
- `pom.xml` : Configuración de Maven con dependencias y plugins.  
- `karate-config.js` : Configuración global de Karate, incluyendo URLs por entorno y generación de emails aleatorios.
---

## Requisitos
- **Java JDK 8** o superior  
- **Maven 3.8+**  
- Conexión a internet para descargar dependencias  
---

## Configuración

1. Clonar el repositorio:

```bash
git clone https://github.com/fgbenavidesg-NNT/RetoQABack.git
cd RetoQABack
```
## Ejecución de pruebas

# Ejecutar todas las pruebas
```bash
mvn clean test
```
# Ejecutar escenario
```bash
mvn test -D"karate.options=--tags @listarUsuarios"
```
# Casos negativos
```bash
mvn test -D"karate.options=--tags @unhappyPath"
```
# Casos positivos
```bash
mvn test -D"karate.options=--tags @happyPath"
```

