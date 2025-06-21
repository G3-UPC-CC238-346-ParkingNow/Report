#### 6.2.1.7. Software Deployment Evidence for Sprint Review.

Durante este Sprint (Sprint 1), logramos desarrollar el landing page de PARKINGNOW. Su propósito principal es atraer a potenciales clientes y mostrar la esencia de nuestro servicio. Respecto al Main de la landing page, optamos por utilizar GitHub page para su despliegue. Aunque la Aplicacion movil aún no está completamente terminada, consideramos que el progreso actual de nuestra landing page cumple con el requisito principal de transmitir nuestro servicio de forma clara y estilizada.

Durante este Sprint desplegamos el backend e hizimos las pruebas requeridas 

### Inicio del despliegue
Empezamos logueandonos en la plataforma

![startdeployment](/Assets/chapter-6/deploy_start.png)

### Configuracion de la base de datos
Configuramos una base de datos con NEON 

![configdb](/Assets/chapter-6/config_db.png)

### Cambios finales para producción
Se agregan cambios a producción para la ejecucion correcta de Nest en la plataforma

![configdb](/Assets/chapter-6/cambios_produccion.png)

Obtenemos el log del despliegue y comprobamos la conexion a la base de datos

![configdb](/Assets/chapter-6/comprobacion_despliegue.png)

### Comprobacion del despliegue

Revision de los logs de despliegue

![configdb](/Assets/chapter-6/tail_1.png)

Sin conflicto, despliegue exitoso

![configdb](/Assets/chapter-6/tail_2.png)

Detalles de la aplicación en la plataforma

![configdb](/Assets/chapter-6/heroku_details.png)

### Testeo de la aplicación

Testeo de la aplicacion en producción 

![configdb](/Assets/chapter-6/test_app.png)

Verificamos la creacion de registros en la base de datos de producción

![configdb](/Assets/chapter-6/test_exitoso.png)

Comprobacion de las apis abieretas

![configdb](/Assets/chapter-6/api_abierta.png)
