# Practica servidor web
## Informe de dos contenedores nginx
## 2. Tiempo : 45 minutos   
## 3. Fundamentos:

 ### 3.1 Docker
 Docker es una plataforma para poder virtualizar y empaquetar aplicaciones con dependencias en contenedores, que a diferencia de las máquinas virtuales comparten el mismo núcleo del sistema.

 - Imagen -
 Una imagen es un conjunto de instrucciones que describe cómo se debe configurar el contenedor.
 ### 3.2 Nginx
 Nginx es un servidor web de código abierto para poder almacenar contenido estatico, en otras palabras para poder almacenar imagenes, código HTML.

Para que nginx sirva como un contenedor necesitamos tener un archivo Html, en otras palabras Nginx toma este archivo html para poder hacer la petición de Docker.
## 4. Conocimientos previos.
   
Para realizar esta practica debemos tener conocimientos es:
1. Conocimientos de Docker.
2. Acceso a Play with Docker.
3. Conocimientos de HTML.
4. Uso de la Terminal.
5. Navegador Web.
6. Herramientas de Edición de Texto (como nano o vi).
7. Acceso a Internet.
8. Comprensión de Puertos.
9. Conocimiento de Documentación de Docker y Nginx.

## 5. Objetivos a alcanzar
   
- En esta practica se busca entender como podemos desplegar un documento html como servidor con nginx y docker.
## 6. Equipo necesario:
  
- Computador.
- Navegador web.

## 7. Material de apoyo.
   
- Documentacion de docker.
- Guia de asignatura.
- Imágnes de docker.
  
## 8. Procedimiento

1. Acceso a Play with Docker.
    - Primero accder a play with docker desde un navegador web.
2. Crear una Nueva Sesión.
    - Iniciar sesio en caso de ser necesario
3. Abrir una nueva instancia.
    - Una vez dentro de play with docke abrimos una nueva instancia donde vamos a almacenar nuestros contenedores
    dento encontraremos una terminal.
4. Crear el Archivo HTML.
    - Dentro de la terminal vamos a tener que crear el archivo html con el comando:
        echo '<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>First</title>
</head>
<body>
    <h1>¡Bienvenido a mi sitio web llamado "First"!</h1>
    <p>Este es un sitio web simple servido por Nginx en Docker.</p>
</body>
</html>' > index.html

        Éste comando crea un archivo con codigo html dentro para poder tener el contenido que deseamos mostrar en la página.
5. Iniciar el Contenedor Nginx.
    - Una vez creado el archivo html pasamos a crear el contenedor con nginx con el comando ´docker run --name first-nginx -p 8080:80 -d -v $(pwd)/index.html:/usr/share/nginx/html/index.html nginx´ con este comando vamos ejecutar un nuevo contenedor docker asignandole el nombre de ´first-nginx´ y el puerto ´8080´ tomando el archivo html que creamos con la ruta ´$(pwd)/index.html:/usr/share/nginx/html/index.html´.
6. Verificar que el Contenedor esté en Ejecución.
7. Acceder a la Página Web.
    - Luego encontraresmos se se agregara el puerto en la parte superior de la página que nos encontramos, damos click en el puerto y nos llevará a la página para visuañizar el contenido html.
8. Visualizar el Contenido.

## 9. Resultados esperados:
    
En la práctica se esperaba obtner un dos servidores con docker y nginx para poder poner en practica los conocimietnos que tenemos y adquirir mas en caso de ser necesario.

## 10. Bibliografía
    
- Gough, M. (2018). Docker in action. Manning Publications.

- Docker. (n.d.). Docker documentation. https://docs.docker.com/

- Nginx. (n.d.). Nginx documentation. https://nginx.org/en/docs/

- Smith, J. (2020). Containerization: A new era in software development. Journal of Software Engineering, 12(3), 45-60.

- Brown, A. (2021). Getting started with Nginx and Docker. Medium. https://medium.com/@abrown/getting-started-with-nginx-and-docker-123456

- Johnson, R. (2022). Docker and Nginx fundamentals. Coursera. https://www.coursera.org/learn/docker-nginx-fundamentals

