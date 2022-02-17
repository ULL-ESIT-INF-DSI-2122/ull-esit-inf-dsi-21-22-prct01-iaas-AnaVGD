# **Práctica 1 - Configuración de máquina virtual en el IaaS**

Gestión de proyectos informáticos
<br />
Ana Virginia Giambona Díaz
<br />
Alu0101322650@ull.edu.es
<br />


## Índice
- [Objetivo](#Objetivo)
- [Algunas tareas previas](#Algunas-tareas-previas)
- [Configuración de la máquina virtual en el IaaS](#Configuración-de-la-máquina-virtual-en-el-IaaS)
- [Instalación de git y Node.js en la máquina virtual del IaaS](#Instalación-de-git-y-Node.js-en-la-máquina-virtual-del-IaaS)
<br />
<br />

## Objetivo

El objetivo de esta practicas es configurar la maquina virtual disponibles en el servicio IaaS de la ULL, también se inhalaran y configuraran las diferentes herramientas necesarios para trabajar en la asignatura.
<br />
<br />


## Algunas tareas previas

1. Cumplimente la encuesta de elección de grupo de trabajo. Pertenezco el grupo H como se puede observar.
![grupo de trabajo](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2020-44-54.png?raw=true)
<br />

2. Como se puede ver realice la encuesta sobre expectativas y conocimientos previos.
![Encuesta](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2020-43-52.png?raw=true)
<br />

4. Solicite los beneficios de estudiantes de GitHub Education.
![GitHub Education](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2020-51-27.png?raw=true)
<br />

6. Acepté la asignación de GitHub Classroom asociada a esta práctica.
![GitHub Classroom](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2020-55-16.png?raw=true)
<br />

7. Realice los cursos: 
* [GitHub Pages](https://lab.github.com/githubtraining/github-pages)

![GitHub Pages](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2021-54-40.png?raw=true)
<br />

* [Communicating using Markdown](https://lab.github.com/githubtraining/communicating-using-markdown)

![using Markdown](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2021-55-30.png?raw=true)
<br />
<br />

## Configuración de la máquina virtual en el IaaS

En este apartado nos centraremos en configurara la maquina virtual en el IaaS por lo que primero accedo al servicio IaaS de la ULL

<div>
<img src="https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%202022-02-16%20233918.png?raw=true" width="280" height="300"/>
</div>
<br />

Posteriormente seleccionamos la maquina virtual que se nos fue asiganada para la asignatura, que en mi caso es DSI-24. 
<div>
<img src="https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%202022-02-17%20175245.png?raw=true" width="360" height="300"/>
</div>
<br />

Luego nos dirigiremos a la Consola VNC (explorador), donde introduciremos como usuario y contraseña, usuario y usuario, qu posteriormente nos pedirá que cambiemos la contraseña.

![Consola VNC](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2022-11-36.png?raw=true)

![Consola VNC](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2018-32-08.png?raw=true)
<br />

A continuación de realizar esto, debemos conocer la IP asignada a la interfaz de red de la máquina, por lo que debemos introducir el siguiente comando:

```
ifconfig -a
```
![ifconfig -a](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2018-40-18.png?raw=true)

Como se nos muestra en la imagen podemos ver que nuestra IP es `10.6.129.86`. Con esta IP ya podemos conectarnos por SSH a la máquina, de forma que en la terminal introducimos el siguiente comando.

```
ssh usuario@10.6.129.86
```

Nos saldrá el siguiente mensaje al que introduciremos ***yes***
![Mensaje](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2019-26-10.png?raw=true)

Tras esto nos pedirá nuestra contraseña (la nueva)
![ssh](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2018-49-47.png?raw=true)
<br />


Luego de realizar las configuración previas ahora podemos modificar el nombre de host de la maquina virtual, de la siguiente manera.
![nombre de host](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2018-52-19.png?raw=true)

Como podemos ver en la imagen he cambiado el nombre del host de la maquina **ubuntu** por **iaas-dsi-AnaVGD**. Ademas debemos realizar cambios en el fichero host. 
![fichero host](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2018-55-15.png?raw=true)

Como se observa en en la imagen cambiamos el nombre **ubuntu** por **iaas-dsi-AnaVGD**.
<br />

Antes que nada actualizamos el software de la máquina.
![apt update](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2019-08-44.png?raw=true)
<br />

Ahora nos disponemos a reiniciar la maquina
![reiniciar la maquina](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2019-09-52.png?raw=true)
<br />


A continuación, modificare el fichero host de mi maquina local para incluir información de conexión a la maquina virtual, de forma que no tenga que recordar la IP de mi maquina virtual.
![Host antes](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2019-21-58.png?raw=true)

![Host despues](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2019-22-08.png?raw=true)
<br />


Configuro en mi maquina local la infraestructura de la clave pública-privada.
![clave pública-privada](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2019-24-01.png?raw=true)

Tras haber generado las claves ejecuto el comando `ssh-copy-id usuario@iaas-ds` que me permite copiar mi clave pública desde la maquina local a la maquina virtual. 
![ssh-copy](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2019-40-05.png?raw=true)
<br />

Siguiendo la instrucciones que vemos en la imagen introducimos `ssh 'usuario@iaas-dsi-AnaVGD'` para realizar el inicio de sesión en la maquina virtual
![ssh](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2019-45-58.png?raw=true)

Como podemos observar he accedido a la maquina virtual sin necesidad de introducir ninguna contraseña y también vemos que el prompt de la maquina virtual ha cambiado por `iaas-dsi-AnaVG`
<br />

A su vez, podemos cambiar el nombre de usuario *usuario* de la maquina virtual a la hora de conectarse via SSH, pudiendo iniciar una conexión SSH simplemente indicando el nombre de la máquina virtual.

![nombre de usuario](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2019-52-43.png?raw=true)

![nombre de usuario](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2019-54-00.png?raw=true)
<br />

Genero las claves pública-privada en mi maquina virtual, del mismo modo como lo realice anteriormente
![claves pública-privada](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2019-58-45.png?raw=true)
<br />
<br />

## Instalación de git y Node.js en la máquina virtual del IaaS
<br />

Instalo git en mi máquina virtual 
![git](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2020-00-21.png?raw=true)
<br />

Posteriormente configuro git ejecutando los siguientes comandos 
![configuro git](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2020-01-23.png?raw=true)


A continuación configuro el prompt de la terminal para que aparezca la rama actual en la que me encuentro, cuando accedo a algún directorio que resulta estar asociado a un repositorio git. Por lo que descargo el script [git prompt](https://github.com/git/git/blob/45fe28c951c3e70666ee4ef8379772851a8e4d32/contrib/completion/git-prompt.sh)
![git prompt](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2020-06-55.png?raw=true)

Como pueden observar lo que hice fue a partir del script [git prompt](https://github.com/git/git/blob/45fe28c951c3e70666ee4ef8379772851a8e4d32/contrib/completion/git-prompt.sh) añadí las siguientes dos lineas al final

```
source ~/.git-prompt.sh
PS1='\[\033]0;\u@\h:\w\007\]\[\033[0;34m\][\[\033[0;31m\]\w\[\033[0;32m\]($(git branch 2>/dev/null | sed -n "s/\* \(.*\)/\1/p"))\[\033[0;34m\]]$'
```

Luego ejecuté el comando `exec bash -l` permitiéndome reiniciar la terminal. Podemos ver que el prompt ha cambiado.
<br />

Para comprobar que el prompt muestra correctamente la rama actual de trabajo, debemos acceder a un directorio asociado a un repositorio, posteriormente añado la clave pública de la máquina virtual en la configuración de las claves de mi GitHub, facilitándome de este modo el trabajo con los repositorios remotos y permitiéndome clonar alguno de los repositorios, por lo tanto debo copiar la clave publica de mi maquina virtual y crear una nueva SSH key en mi cuenta de GitHub introduciendo en ella la clave pública de mi maquina virtual.

![claves de mi GitHub](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2020-16-32.png?raw=true)
<br />
<br />


Clono el repositorio de la practica
![Clonado del repo](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2020-31-37.png?raw=true)

Como se observa en la imagen se ha clonado el repositorio de GitHub correctamente sin tener que introducir ninguna credencial, asi como accedo al directorio asociado al repositorio git y se puede ver en el prompt del sistema (entre paréntesis) la rama actual de trabajo (main)
<br />

Instalo el Node Version Manager (nvm), [Node Version Manager (nvm)](https://github.com/nvm-sh/nvm.git), el gestor de versiones de Node.js, este me permite la ejecución de código desarrollado en JavaScript y variantes.
![Node Version Manager](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2020-39-33.png?raw=true)
<br />
<br />


Como se observa he instalado nvm satisfactoriamente, por lo que a continuación instalo la versión más reciente de Node.js , en mi caso ya lo tenia instalado:
![Node.js](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2020-41-20.png?raw=true)
<br />
<br />

Tras realizar todas estas configuraciones ya tendría configurada mi maquina pera realizar las tareas de la asignatura.