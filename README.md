# Unix tour

Se supone que antes de este tour se tienen algunos conceptos básicos de comandos unix ```ls, cp, mv, ps,```.

Vamos a utilizar [vagrant](http://docs.vagrantup.com/v2/getting-started/index.html) para instalarlo en nuestro sistema operativo y no tocar nuestro propio sistema. Vagrant os pedirá que instaléis también [VirtualBox](https://www.virtualbox.org/wiki/Downloads). 

Una vez instalado con estos tres commandos, tendréis virtualizada e instalada una máquina con Ubuntu y os encontraréis dentro de su consola con el nombre de usuario ```vagrant```. 

```
vagrant init hashicorp/precise32
vagrant up
vagrant ssh
```
![Consola inicial](img/consola-inicial.png)

# Utilidades

Cambia mucho de una persona a otra, qué cosas son útiles y cuales no. Yo voy a listar algunos. Todos ellos instalables utilizando el comando: 

```sudo apt-get install <selected package>```

*Nota:* Probablemente si es la primera vez que ejecutáis ```apt-get``` tendréis primero que hacer una actualización con ```sudo apt-get update ``

#### Lista de mis utilidades:


+ ```vim``` : Editor de texto algo más completo que vi. 

# Usuarios

+ ```whoami``` : Con este comando sabremos el usuario con el que estamos conectado, en este caso ```vagrant```. Aunque también lo podemos saber viendo el nombre que muestra la consola (como en la imagen anterior) antes de la ```@```.

Pero es que como en cualquier sistema operativo, existen otros usuarios, podemos crearlos, podemos cambiar, ... Esos usuarios se guardan en un fichero especial que podemos visualizar usando ```cat /etc/passwd```. Obtendremos entonces algo como esto: 

```
messagebus:x:102:105::/var/run/dbus:/bin/false
ntp:x:103:108::/home/ntp:/bin/false
sshd:x:104:65534::/var/run/sshd:/usr/sbin/nologin
vagrant:x:1000:1000:vagrant,,,:/home/vagrant:/bin/bash
vboxadd:x:999:1::/var/run/vboxadd:/bin/false
statd:x:105:65534::/var/lib/nfs:/bin/false
```

**¿Qué es esto?** ```Cada linea``` es un usuario. Y en cada linea el símbolo ```:``` separa diferentes propiedades de cada usuario que se explican genial en [este documento](http://www.cyberciti.biz/faq/understanding-etcpasswd-file-format/). 

# Vim 

Abro esta sección porque realmente un editor de texto y vim, es algo que se utiliza mucho y está bien saber algunas cosas más. 

*Nota:* Os recomiendo que juguéis antes un rato con ```vimtutor```que podéis ejectura directamente como si fuera un comando.

Una vez dentro de vim, podéis lanzar el comando: 

+ ```:set number``` para ver el número de lineas a la izquierda
+ ```:syntax on``` para colorear la sintáxi de los diferentes lenguajes
+ ```:set tabstop=4``` definir la longitud de los tabuladores
+ ```:set expandtab``` definir los tabuladores como espacios

#### Customizar VIM

Algunas de las opciones que he contado antes se puede añadir para que se abran por defecto. ¿Cómo? Debes crear un archivo en tu carpeta de usuario ```~``` que se llame ```.vimrc```. 

Allí dentro puedes añadir en lineas separadas las instrucciones (como ```:set number```) que quieres que se ejecuten cada vez que se abra vim. 


# Otros

+ [Organización Ficheros UNIX](http://en.wikipedia.org/wiki/Unix_filesystem)
+ [Bash Guide for Beginners](http://www.tldp.org/LDP/Bash-Beginners-Guide/html/sect_01_04.html)
+ [UNIX Find A File Command](http://www.cyberciti.biz/faq/howto-find-a-file-under-unix/)
+ [UNIX Command NC](http://www.tutorialspoint.com/unix_commands/nc.htm)
