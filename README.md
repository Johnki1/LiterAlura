# Literalura - Aplicación de Consola para Consultar y Almacenar Libros

## Descripción

Literalura es una aplicación de consola desarrollada en Java que se conecta a la API de Gutendex para buscar libros y guardarlos en una base de datos PostgreSQL. Además, permite consultar y visualizar información sobre libros y autores almacenados en la base de datos.

La aplicación utiliza una arquitectura simple y eficiente, implementando patrones de diseño como Repositorio y Servicio para separar las responsabilidades y facilitar la escalabilidad y mantenibilidad del código.

## Funcionalidades

La aplicación ofrece las siguientes funcionalidades:

- **Buscar Libro por Título**: Permite buscar un libro por su título en la API de Gutendex y guardarlo en la base de datos si no existe.
- **Listar Libros Registrados**: Muestra todos los libros almacenados en la base de datos.
- **Listar Autores Registrados**: Muestra todos los autores almacenados en la base de datos.
- **Listar Autores Vivos en un Determinado Año**: Permite listar autores que estén vivos en un año específico.
- **Listar Libros por Idioma**: Permite listar libros disponibles en un idioma específico.
- **Ver Top 10 con Más Descargas de la API**: Muestra los 10 libros más descargados desde la API de Gutendex.
- **Ver Top 10 con Más Descargas de la Base de Datos**: Muestra los N libros más descargados almacenados en la base de datos.
- **Consultar Autor por Nombre**: Permite buscar autores por su nombre en la base de datos.
- **Listar Autores por Años de Fallecimiento**: Permite listar autores que fallecieron después de un año específico.

## Requerimientos

- Java 8 o superior.
- Base de datos PostgreSQL.
- Clave de API de Gutendex.

## Configuración

Antes de ejecutar la aplicación, asegúrate de configurar correctamente los siguientes parámetros en el archivo `application.properties`:

```
spring.application.name=literalura

spring.datasource.url=jdbc:postgresql://${DB_HOST}/literalura
spring.datasource.username=${DB_USER}
spring.datasource.password=${DB_PASSWORD}
spring.datasource.driver-class-name=org.postgresql.Driver
hibernate.dialect=org.hibernate.dialect.HSQLDialect

spring.jpa.hibernate.ddl-auto=update

spring.jpa.show-sql=true
spring.jpa.format-sql=true
```

Reemplaza `${DB_HOST}`, `${DB_USER}`, `${DB_PASSWORD}`  con los valores correspondientes según tu entorno.

## Instalación y Ejecución

1. Clona este repositorio en tu máquina local.
2. Configura correctamente las propiedades de la base de datos en `application.properties`.
3. Ejecuta la aplicación desde tu IDE o mediante el comando `mvn spring-boot:run`.

## Uso

Una vez que la aplicación esté en funcionamiento, sigue las instrucciones en la consola para utilizar las diferentes funcionalidades del programa. Selecciona la opción deseada ingresando el número correspondiente y sigue las indicaciones para interactuar con la aplicación.

## Contribución

Las contribuciones son bienvenidas. Si deseas contribuir a este proyecto, sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una rama para tu funcionalidad (`git checkout -b feature/AmazingFeature`).
3. Realiza tus cambios y haz commit de ellos (`git commit -m 'Add some AmazingFeature'`).
4. Haz push de tu rama al repositorio remoto (`git push origin feature/AmazingFeature`).
5. Abre un pull request.

## Autor

- Nombre: [John Alzate]
- Contacto: [garciakider@gmail.com]
