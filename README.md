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
