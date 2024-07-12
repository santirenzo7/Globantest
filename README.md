# Globantest

Conexión a la Base de Datos: Se establece una conexión a la base de datos mediante SQLAlchemy.
Consulta SQL: Se define una consulta SQL que calcula el promedio de contrataciones en 2021 y luego obtiene los departamentos que han contratado más que este promedio.
Ejecución de la Consulta: La consulta SQL se ejecuta utilizando pandas para obtener los resultados en un DataFrame.
Impresión del Listado: Se imprime el listado en la consola.
Tecnologías Utilizadas
Lenguaje de Programación: Python
Bibliotecas Utilizadas:
pandas: Para la manipulación y análisis de datos.
SQLAlchemy: Para interactuar con la base de datos.
pyodbc: Para la conexión a la base de datos SQL Server.




Bonus Track: Nube, Pruebas Automatizadas y Contenedores
Si bien no implemente la dockerización por no tener las configuraciones ni el entorno necesario de esta manera lo encararia.

Hospedaje en la Nube:

Servicio de Nube Pública: Usaria AWS para hospedar la arquitectura.
Configuración de la Instancia: Crear una instancia de EC2 con una AMI de Ubuntu y configurar los grupos de seguridad necesarios para trafico HTTP, HTTPS y SSH
Subida de la Imagen de Docker a ECR: Subir la imagen de Docker al Elastic Container Registry (ECR) de AWS y ejecutar la imagen en la instancia de EC2.
La aplicación debería estar accesible en la IP pública de mi instancia de EC2.
Pruebas Automatizadas: aca si no tengo mucha experiencia de como realizarla
Contenerización:Puedo utilizar ECS (Elastic Container Service) y ECR (Elastic Cointainer Registry)
Dockerfile: Crear un Dockerfile para contenedizar la aplicación.
Construcción y Ejecución del Contenedor: Construir la imagen de Docker y ejecutar el contenedor localmente para verificar su correcto funcionamiento.

Navego a Amazon ECR,Creo el repositorio para mi imagen docker, construyo localmente mi imagen y la subo a ECR.
Luego en ECS creo la definición de la tarea especificando la imagen Docker almacenada en ECR.
Configuro los detalles del servicio,escalado,etc.
Implemento el servicio clusterizado de ECS.
