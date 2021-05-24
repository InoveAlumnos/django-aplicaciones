![Inove banner](/inove.jpg)
Inove Escuela de Código\
info@inove.com.ar\
Web: [Inove](http://inove.com.ar)

---

# Django - Aplicaciones
En este repositorio encontrarán los siguientes archivos:

__Ejemplos que el profesor mostrará en clase__\
docker-compose.yml

---

# Comandos útiles 🐋

### 1. Correr el proyecto
Siempre en el mismo directorio del archivo *docker-compose.yml*
**$** `docker-compose up`

### 2. Correr la línea de comandos dentro del contenedor

**$** `docker exec -i -t [nombre_del_contenedor] bash`

Para el caso de este ejemplo:

**$** `docker exec -i -t modulo_2 bash`

Nos va a devolver a nuestra consola, una consola dentro del contenedor de software.

### 3. Instalar la librería de django
Tenemos que estar dentro del contenedor con el comando anterior, luego, tenemos que utilizar el gestor de paquetes de Python, PIP para instalarlo.
Vamos a utilizar la versión 3.2.2 de django.

**$** `pip install Django==3.2.2` 

### 4. Crear un proyecto de Django
Para ello tenemos que estar dentro del contenedor de software (comando N°2)
Y luego nos dirigimos a la carpeta raíz de nuestro proyecto:

**$** `cd opt/back_end` 

Una vez dentro ejecutamos el comando:

**$** `django-admin startproject modulo_2` 

### 5. Crear una aplicación dentro del proyecto
Tenemos que ir a la carpeta donde se encuentra el archivo *manage.py*  
(Siempre dentro de nuestro contenedor de software - Comando N°2)  

**$** `cd opt/back_end/modulo_2` 
Y ejecutar el comando:  

**$** `python manage.py startapp mi_app` 

### 6. Iniciar el servidor
(Siempre dentro de nuestro contenedor de software - Comando N°2)  
Tenemos que ir a la carpeta donde se encuentra el archivo *manage.py*  

**$** `python manage.py runserver 0.0.0.0:8000`  

### 7. Detener la ejecución de nuestro contenedor y nuestro servidor
Tenemos que estar en la terminal que nos muestra los mensajes del servidor, tomada por el contenedor.
Tan solo con el comando `ctrl + c`  se detiene la ejecución de nuestro contenedor.  

Una forma alternativa es con el siguiente comando en la terminal del host:

**$** `docker stop modulo_2`  

O también puede ser con docker-compose:
Tenemos que estar en la carpeta que contiene el archivo *docker-compose.yml* y hacer:


**$** `docker-compose down`  

---
# Consultas
alumnos@inove.com.ar

