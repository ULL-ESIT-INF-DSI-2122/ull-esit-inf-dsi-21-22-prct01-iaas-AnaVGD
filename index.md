# Práctica 1 - Configuración de máquina virtual en el IaaS

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

Posteriormente seleccionamos la maquina virtual que se nos fue asiganada para la asignatura, que en mi caso es DSI-24. 
<div>
<img src="https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%202022-02-17%20175245.png?raw=true" width="360" height="300"/>
</div>

Luego nos dirigiremos a la Consola VNC (explorador), donde introduciremos como usuario y contraseña, usuario y usuario, qu posteriormente nos pedirá que cambiemos la contraseña.

![Consola VNC](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2022-11-36.png?raw=true)

![Consola VNC](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2018-32-08.png?raw=true)
<br />
<br />


Luego de realizar esto debemos conocer la IP asignada a la interfaz de red de la máquina, por lo que debemos introducir el siguiente comando:

`ifconfig -a`
<br />

![ifconfig -a](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2018-40-18.png?raw=true)

Como se nos muestra en la imagen podemos ver que nuestra IP es `10.6.129.86`. Con esta IP ya podemos conectarnos por SSH a la máquina, de forma que en la terminal introducimos el siguiente comando.

`ssh usuario@10.6.129.86`

Nos saldrá el siguiente mensaje al que introduciremos yes

![ssh](https://github.com/AnaVGD/Imagenes/blob/main/Captura%20de%20pantalla%20de%202022-02-17%2018-49-47.png?raw=true)


Tras esto nos pedir nustra contraseña (la nueva)

![IaaS]()

Luego de rializar las configuracions previas ahora podemos modificar el nombre de host de la maquina virtual, de la siguiente manera.

![IaaS]()

Como podemos ver en la imagen he cambiado el nombre del host de la maquina **ubuntu** por **iaas-dsi-AnaVGD**. Ademas debemos realizar cambios en el fichero host. 


![IaaS]()

Como se observa en en la imagen cambiamos el nombre ubuntu por **iaas-dsi-AnaVGD**.

ANtes que nada autualizamos el software de la máquina.

![IaaS]()

Ahora nos disponemos a reiniciar la maquina

![IaaS]()

A continuación, modificare mi fichero host de mi maquina local para incluir informacion de conexion a la maquina virtual, de forma que no tenga que recordare la IP de la maquina virtual.

![IaaS]()
![IaaS]()

Configuro en mi maquina local la infraestructura de la clave pública-privada.
![IaaS]()

TRas haber generado las claves ejecuto el comando `ssh-copy-id usuario@iaas-ds` que me permite copiar mi clave pública desde la maquina local a la maquina virtual. 

![IaaS]()

Sigiendo la intrucciones que vemos en la imagen introducimos `ssh 'usuario@iaas-dsi-AnaVGD'` para realizar el inicio de sesion en la maquina virtual

![IaaS]()

Como podemos observar he accedido a la maquina virtual sin necesiadad de introducir nunguna contraseña y tambien vemos que el promot de la maquina virtual ha cambiado por `iaas-dsi-AnaVG`.

A su vez, podemos cambiar el nombre de usuario *usuario* de la maquina virtual a la hora de conectarse via SSH, pudiendo iniciar una conexión SSH simplemente indicando el nombre de la máquina virtual.

![IaaS]()

Genero las claves pública-privada en mi maquina virtual, del mismo modo como lo realice anteriormente


![IaaS]()

## Instalación de git y Node.js en la máquina virtual del IaaS

Instalo git en mi maquina virtual 

![IaaS]()

Posteriormente configuro git ejecutando los siguientes comandos 

![IaaS]()


A continuacion configuro el promp de la terminal para que aparezca la rama actual en la que me encuentro cuando accedo a algún directorio que resulta estar asociado a un repositorio git. Por lo que descrago el script git prompt [git prompt](https://github.com/git/git/blob/45fe28c951c3e70666ee4ef8379772851a8e4d32/contrib/completion/git-prompt.sh)

![IaaS]()

Como pueden observar lo que hice fue a partir del script [git prompt](https://github.com/git/git/blob/45fe28c951c3e70666ee4ef8379772851a8e4d32/contrib/completion/git-prompt.sh) lo modifique añadiendoles las siguientes dos lineas al final

`source ~/.git-prompt.sh
PS1='\[\033]0;\u@\h:\w\007\]\[\033[0;34m\][\[\033[0;31m\]\w\[\033[0;32m\]($(git branch 2>/dev/null | sed -n "s/\* \(.*\)/\1/p"))\[\033[0;34m\]]$'`

Luego ejecute el comando `exec bash -l` permitiednome reiniciar la terminal. Podemos ver que el prompt ha cambiado.

Para comprobarque el prompt muestra correctamente la rama actual de trabajo cuando accedemos a un directorio asociado a un repositorio, tengo que añadir  la clave pública de la máquina virtual en la configuración de las claves de mi GitHub, facilitandome el trabajo con los repositorios remostos y permitiednome clonar alguno de los repositorios, por lo tanto debo copiar la clave publica de mi maquina virtual y creear una nueva SSH key en mi cuenta de GitHub copiendo en ella la clave pública de mi maquina virtual.

![IaaS]()

Clono el repositorio de la practica

![IaaS]()

Como se observa en la imagen se ha clonado el repositorio de GitHub correctamente sin tener que introducir ninguna credencial, asi como accedo al directorio asociado al repositorio git y se puede ver en el pront del sistema (entre parentesis) la rama actual de trabajo (main)


Instalo el Node Version Manager (nvm), [Node Version Manager (nvm)](https://github.com/nvm-sh/nvm.git), el gestor de versiones de Node.js, este me permite la ejecución de código desarrollado en JavaScript y variantes.

![IaaS]()

Como se observa he intalado nvm satisfactoriamente, por lo que a continuacion intalo la versión más reciente de Node.js , en mi caso ya lo tenia instalado:


![IaaS]()