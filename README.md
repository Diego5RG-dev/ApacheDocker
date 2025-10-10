# ApacheDocker
<h1 align="center">   Tareas de docker con Apache </h1> <br>
<p align="center">
    <img alt="logo" title="logo" src="https://github.com/Diego5RG-dev/ApacheDocker/blob/main/recursosDocker2/logo.jpg "width="450">
</p>

---
Descarga la imagen 'httpd' y comprueba que está en tu equipo
---

Utilizando el siguiente comando:

    docker pull httpd:2.4

Con esto, si ahora listamos las imágenes, veremos que esta nos aparece en el equipo.

<p align= center>
  <img alt="logo" title="logo" src="https://github.com/Diego5RG-dev/ApacheDocker/blob/main/recursosDocker2/1_2.png "width="75%">
</p>

---
Crea un contenedor con el nombre 'dam_web1'.
---

Ya con el comando que usamos en la práctica anterior, podemos crear el contenedor al cual, para futuro, le asignaremos el puerto:

    docker run -d --name dam_web1 -p 8080:80 httpd:2.4

Con esto, podemos ver si hacemos un listado de los contenedores.

<p align= center>
  <img alt="logo" title="logo" src="https://github.com/Diego5RG-dev/ApacheDocker/blob/main/recursosDocker2/2.png "width="75%">
</p>

---
Si quieres poder acceder desde el navegador de tu equipo, ¿que debes hacer?
---

Aquí ya es donde contamos con la ventaja de haber hecho anteriormente la configuración de puertos, porque simplemente poniendo la dirección del host en el buscador nos aparecerá la página predeterminada de httpd:

        http://localhost:8080/

Y ahora sí, si vamos al buscador, nos aparecerá esta imagen.

<p align= center>
  <img alt="logo" title="logo" src="https://github.com/Diego5RG-dev/ApacheDocker/blob/main/recursosDocker2/3.png ">
</p>

---
Utiliza bind mount para que el directorio del apache2 'htdocs' esté montado un directorio que tu elijas.
---

Con este apartado tuve que volver a crear el contenedor, y esta vez hacerlo mediante el Bind Mount, como pide la tarea, con el comando:


        docker run -d --name dam_web1 -p 8080:80 -v ~/docker:/usr/local/apache2/htdocs httpd:2.4

Con esto, podemos ver si hacemos un listado de los contenedores

<p align= center>
  <img alt="cuarta" title="cuarta" src="https://github.com/Diego5RG-dev/ApacheDocker/blob/main/recursosDocker2/4.png "width="75%">
</p>
