# Instalación de IntelliJ

## Natalia Rolón Leal

## Capturas de la instalación
![img_1](/img/1.JPG)

![img_2](/img/2.JPG)

![img_3](/img/3.JPG)

![img_4](/img/4.JPG)

![img_5](/img/5.JPG)

![img_6](/img/6.JPG)


# Mi Primer Spring Boot (holamundo)

Esta fue una actividad práctica para la creación, ejecución y prueba de una aplicación basada en Spring Boot con múltiples endpoints REST, aplicando controladores, servicios, configuración externa, beans e inyección de dependencias.


### 1. Estructura del proyecto

![img_23](/img/23.JPG)


### 2. Ejecución de la aplicación

![img_7](/img/7.JPG)

![img_8](/img/8.JPG)

![img_9](/img/9.JPG)

![img_10](/img/10.JPG)

![img_12](/img/12.JPG)


## 3. Pruebas de Endpoints en Postman

![img_13](/img/13.JPG)

![img_14](/img/14.JPG)


Endpoint /api/hola:

![img_15](/img/15.JPG)


Endpoint /saludo:

![img_16](/img/16.JPG)


Endpoint /config:

![img_17](/img/17.JPG)


## 4. Pruebas de Endpoints en Insomnia

Endpoint /api/hola:

![img_18](/img/18.JPG)


Endpoint /saludo:

![img_19](/img/19.JPG)


Endpoint /config:

![img_20](/img/20.JPG)


## 5. Pruebas de Retos y Errores

Reto de Método Equivocado (404 Not Found)

![img_21](/img/21.JPG)


Reto de Método Equivocado (405 Method Not Allowed):

![img_22](/img/22.JPG)


Reto de la Anotación @Service faltante:

![img_11](/img/11.JPG)


## 6. Preguntas Teóricas

¿Qué diferencia hay entre @RestController y @Service, y por qué Spring puede entregar el servicio al controlador sin usar new?

@RestController: Es una anotación especializada para la capa web. Indica que la clase es un controlador que gestionará peticiones HTTP (como GET, POST, etc.) y que sus métodos devolverán datos directamente (generalmente en formato JSON o texto plano) en lugar de renderizar vistas HTML tradicionales.

@Service: Es una anotación para la capa de lógica de negocio. Marca la clase como un componente gestionado por el contenedor de Spring (un Bean), encapsulando las reglas y operaciones del sistema lejos de la infraestructura web.

¿Por qué Spring puede entregar el servicio sin usar new?
Esto es posible gracias al contenedor de Inversión de Control (IoC) y Inyección de Dependencias (DI) de Spring. Cuando la aplicación arranca, Spring escanea los paquetes buscando anotaciones como @Service o @Component. Al encontrar MiServicio con @Service, Spring instancia automáticamente ese objeto y lo almacena en su contenedor interno (llamado contexto de Spring).

Cuando Spring instancia el SaludoController, detecta que este requiere un MiServicio en su constructor (gracias a @Autowired o a la inyección automática por constructor). En lugar de obligar al programador a usar la palabra reservada new MiServicio(), el framework busca el objeto ya creado en su contenedor y se lo inyecta de forma transparente y automática.