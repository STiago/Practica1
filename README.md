# PRÁCTICA 1 : Creación y despliegue de una aplicación en un PaaS
## María Victoria Santiago Alcalá

## Licencia de la aplicación: GPLv3

### - Aplicación
Se trata de una aplicación en php la cual se ocupa de la conversión de una cantidad de peseta a introducir por el usuario, a euros o bien a dólares según su elección. 

### - Elección del PAAS

Para realiza la práctica, he elegido el Paas OpenShift de RedHat por varios motivos los cuales explico a continuación.

Una de las razones es porque da soporte a varios lenguajes de programación que conozco por lo que me facilita la realización de la práctica.

La otra razón es que OpenShift es un producto de computación en la nube de plataforma como servicio de Red Hat, funciona como un servicio que es de código abierto bajo el nombre de "OpenShift Origin", y está disponible en GitHub.

Los desarrolladores pueden usar Git para desplegar sus aplicaciones Web en los diferentes lenguajes de la plataforma.

OpenShift también soporta programas binarios que sean aplicaciones Web, con tal de que se puedan ejecutar en RHEL Linux. Esto permite el uso de lenguajes arbitrarios y frameworks.

OpenShift se encarga de mantener los servicios subyacentes a la aplicación y la escalabilidad de la aplicación como se necesite.

(La información anterior sobre OpenShift ha sido optenida a partir de la Wikipedia y de la página de OpenShift)
https://www.openshift.com/  ,
https://www.openshift.com/


### - Configuración de cliente rhc, creación del proyecto en openshift y aplicación en openshift
En primer lugar, iniciamos sesión en OpenShift, seguidamente en nuestra consola ejecutamos las siguientes líneas de comandos:

- $ sudo apt-get install rubygems 
- $ sudo gem install rhc
- $ sudo gem update rhc
- $ gem update rhc
- $ rhc setup

Seguidamente tras la última órden, nos identificaremos con nuestro correo de la cuenta de OpenShift y su contraseña para permitirle el acceso.
Con lo anterior ya tendríamos terminada la configuración de cliente rhc, por lo que pasamos a crear nuestro proyecto.

$ rhc create-app  practica1 php-5.3

![Ej9](https://dl.dropbox.com/s/p14idd1hkhrayzo/practica1.2.crearapp.png)

Y como podemos observar, podemos ver la aplicación creada en:  practica1-stiago.rhcloud.com


Seguidamente ya en nuestra cuenta de GitHub, procedemos a crear un repositorio nuevo. Le asignaremos el nombre, público y su licencia (GPLv3).
A continuación en nuestro terminal, haremos lo siguiente para clonar nuestro repositorio en nuestro pc y posteriormente subir los ficheros al repositorio creado:

$ git clone https://github.com/STiago/Practica1.git

Después he introducido mis archivos php, html y demás en la carpeta que se ha clonado en mi directorio.

$ git add.
$ git commit -a -m "Practica1IV"
$ git push

![Ej2](https://dl.dropbox.com/s/9xmzfr2kqyr8kms/ivvv.png)


Y con ello ya estaría todo subido y actualizado en nuestro repositorio de github.

Tenemos la alicación funcionando correctamente en la página : http://practica1-stiago.rhcloud.com/

![Ej3](https://dl.dropbox.com/s/43ydleoghqhxdg5/appp.png)


### - Fuentes de información
- https://www.openshift.com/get-started
- https://www.openshift.com/documentation
- http://www.php.net/manual/es/index.php




