# PROYECTO NODEJS
Pasos para la realización del proyecto `Platziverse`.

Para ver el curso completo ingrese a [Platzi/node](https://platzi.com/nodejs/)
___
### Peparando el entorno de desarrollo.

> Instalación en Ubuntu 16.04

- ***NodeJS***

Sólo tenemos que utilizar el gestor de paquetes `apt`. En primer lugar debemos actualizar nuestro índice de paquetes local, y luego instalarla desde los repositorios:

```shell
user@pc:~$ sudo apt-get update
user@pc:~$ sudo apt-get install nodejs
```

También puede instalar `npm`, que es el gestor de paquetes Node.js. Puede hacer esto escribiendo:

```shell
user@pc:~$ sudo apt-get install npm
```

**¿Cómo Instalar Mediante el uso de NVM?**

Una alternativa a la instalación de Node.js a través de `apt` es utilizar una herramienta especialmente diseñada llamada `nvm`, que significa "administrador de versiones Node.js".

Utilizando `nvm`, puedes instalar varias versiones, independientes de Node.js que permitirán controlar su entorno de forma más fácil. No solo se le dará acceso bajo demanda a las nuevas versiones de Node.js, sino que también le permitirá dirigirse a versiones anteriores de las cuales su aplicación pueda depender.

```shell
user@pc:~$ sudo apt-get update
user@pc:~$ sudo apt-get install build-essential libssl-dev
```

Una vez instalados los paquetes de requisitos previos, puede desplegar el script de instalación de `nvm` [desde la página del proyecto en GitHub](https://github.com/creationix/nvm). El número de versión puede ser diferente, pero en general, se puede descargar con `curl`:

```shell
user@pc:~$ curl -sL https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh -o install_nvm.sh
```

Ejecutar el script con `bash`:

```shell
user@pc:~$ bash install_nvm.sh
```

Para acceder a la funcionalidad de NVM, tendrá que cerrar la sesión y volver a iniciarla de nuevo, o puede generar el archivo `~/.profile` para que la sesión actual reconozca los cambios:

```shell
user@pc:~$ source ~/.profile
```

Para ver las versiones disponibles de Node.js:

```shell
user@pc:~$ nvm ls-remote
```

Para instalar una versión en específico de Node.js:

```shell
user@pc:~$ nvm install 10.4.1
```

Al instalar Node.js usando NVM, el ejecutable se llama `node`. Puede ver la versión que esta siendo utilizada actualmente por el shell escribiendo:

```shell
user@pc:~$ node -v
```

Para ver las versiones instaladas:

```shell
user@pc:~$ nvm ls
```

Para utilizar otra versión instalada de Node.js:

```shell
user@pc:~$ nvm use 9.11.1
```

- ***PostgreSQL***

Sólo tenemos que utilizar el gestor de paquetes `apt`, e instalar `postgresql` `postgresql-contrib` `libpq-dev`

```shell
user@pc:~$ sudo apt-get install postgresql postgresql-contrib libpq-dev
```

- ***Redis***

Debemos utilizar el gestor de paquetes `apt` para instalar paquetes previos que nos ayudará a que varios paquetes que dependan de librerías de tipo `C / C++` se ejecuten con normalidad. Primeramente debemos actualizar nuestro índice de paquetes local, y luego instalarla desde los repositorios:

```shell
user@pc:~$ sudo apt-get update
user@pc:~$ sudo apt-get install build-essential tcl
```

Dado que no necesitamos guardar el código fuente, podemos hacer uso del directorio `/tmp`:

```shell
user@pc:~$ cd /tmp
```

Ahora descargamos la última versión estable de Redis:

```shell
user@pc:~$ curl -O http://download.redis.io/redis-stable.tar.gz
```

Lo descomprimimos con el comando `tar`:

```shell
user@pc:~$ tar xzvf redis-stable.tar.gz
```

Ingresamos al directorio `redis-stable` que se extrajo:

```shell
user@pc:~$ cd redis-stable
```

Compilamos los binarios mediante el comando `make`:

```shell
user@pc:~$ make
```

Instalamos los binarios:

```shell
user@pc:~$ sudo make install
```

*Listo :)*

- ***Ansible***

La mejor forma de obtener Ansible para Ubuntu es agregar el PPA (archivo de paquete personal) del proyecto a su sistema. Podemos agregar el PPA Ansible escribiendo el siguiente comando:

```shell
user@pc:~$ sudo apt-add-repository ppa:ansible/ansible
```

Presione `ENTER` para aceptar la adición de PPA. A continuación, debemos actualizar el índice del paquete de nuestro sistema para que esté al tanto de los paquetes disponibles en el PPA. Luego, podemos instalar `ansible`:

```shell
user@pc:~$ sudo apt-get update
user@pc:~$ sudo apt-get install ansible
```

Para saber la versión de `ansible` que instaló.

```shell
user@pc:~$ ansible --version
```

Para más información de la instalación, haz click en la siguiente [Página](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-16-04)

- ***Vagrant***

Es una herramienta gratuita de línea de comandos, disponible para *Windows*, *MacOS X* y *GNU/Linux*, que permite generar entornos de desarrollo reproducibles y compartibles de forma muy sencilla. Para ello, `Vagrant` crea y configura máquinas virtuales a partir de simples ficheros de configuración.

Para descargar `Vagrant` debe visitar la [Página oficial](https://www.vagrantup.com/downloads.html).  
En el caso de *Ubuntu* descargamos el archivo de ***Debian 64-bit***, descarga un archivo `.deb`, para instalarlo:

```shell
user@pc:~$ cd Descargas
user@pc:~$ sudo dpkg -i vagrant_Xx.Xx.Xx_x86_64.deb
```

> Debe reemplazar _Xx.Xx.Xx_ por la versión que descargó.

Para saber la versión de `Vagrant`.

```shell
user@pc:~$ vagrant -v
```
