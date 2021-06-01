# Introducción a Git y Github 2021

Por [Santiago Soler](https://www.santisoler.com/) y Mariana Gomez

| Información | |
| - | ---
Cuándo | [Sábado 5 de Junio 15:00 a 19:00 GMT](https://www.timeanddate.com/worldclock/fixedtime.html?msg=Introducci%C3%B3n+a+Git+%7C+Geolatinas&iso=20210605T12&p1=51&ah=5)
Dónde | Zoom (link en el canal de Slack `#coding-group`)
Notas colaborativas | Etherpad: https://pad.disroot.org/p/2o7i0afvxpe8jcdy
Material | https://swcarpentry.github.io/git-novice-es

## ANTES DEL TALLER

Asegurate de realizar los siguientes pasos *antes del Sábado 5 de Junio*:

1. Tener instalada una aplicación de Terminal
2. Instalar git
3. Instalar un editor de texto
4. Crearse una cuenta en GitHub

Más adelante encontrás instrucciones de cómo realizar estos pasos.

## Acerca del taller

## Configurar nuestra computadora

Acá podrás encontrar instrucciones para configurar tu computadora y tener todo
listo para el taller.
Las instrucciones y los programas que vas a tener que instalar van a variar
dependiendo de tu tu sistema operativo.
Todos los programas que necesitas para el taller se encuentran bajo licencias
de [Software Libre](https://es.wikipedia.org/wiki/Software_libre).

### Aplicación de Terminal

El primer requisito es tener instalada una aplicación de terminal.
La terminal es un programa que nos permite interactuar con la computadora
mediante comandos de texto que introducimos por el teclado.
En vez de tener menús y botones que clickeamos con el mouse, la terminal nos
permite realizar muchísimas tareas a través de comandos.

Cada sistema operativo posee su propia aplicación de terminal.

Windows
: Windows posee una aplicación de terminal que podemos acceder a través de
`cmd` en nuestro menú de inicio. Esa terminal no nos será útil para este
taller, es por ello que vamos a necesitar instalar una distinta, la cual viene
incluida cuando instalemos `git`. Por ende, pasá al siguiente paso.

MacOS
: MacOS viene por defecto con una aplicación llamada `Terminal` a la cual
podemos acceder desde nuestro menú de Aplicaciones. Verifica que la tienes
instalada y que puedes abrirla sin problemas.

Linux
: Las distribuciones de Linux traen una aplicación de terminal preinstalada,
aunque su nombre puede diferir dependiendo de qué entorno de escritorio o qué
distribución estés usando. Podrás encontrarla en el menú de aplicaciones bajo
el nombre `Emulador de Terminal`, `Terminal de GNOME` o `Konsole`.

### Instalar git

Git es el software que vamos a estar explorando durante el taller y por ende
necesitaremos instalarlo.
Las instrucciones de instalación varían en función del sistema operativo que
utilices.

Windows
: Vamos a instalar GitBash que incluye tanto `git` como una aplicación de
terminal y el shell `bash`. Podrás encontrar
[instrucciones detalladas realizadas por Software
Carpentries](https://carpentries.github.io/workshop-template/#shell) sobre cómo
instalarlo.

Mac
: Vamos a instalar `git-osx-installer`, que podemos descargar desde acá:
https://sourceforge.net/projects/git-osx-installer/files/
. Podrás encontrar
[instrucciones detalladas realizadas por Software
Carpentries](https://carpentries.github.io/workshop-template/#git) sobre cómo
instalarlo.

Linux
: En la mayoría de las distribuciones de Linux podemos instalar `git` mediante
el gestor de paquetes. Si usas Ubuntu, Debian o alguna derivada de ellas,
podés instalarlo ejecutando el siguiente comando en la terminal:
`sudo apt install git`.
Si usas Fedora, ejecutá `sudo dnf install git`. Y si utilizás Arch, Manjaro
o derivadas ejecutá: `sudo pacman -S git`.

### Instalar un editor de texto

Durante el taller vamos a utilizar un editor de texto para realizar cambios
a nuestros archivos. No es necesario que instalemos un editor de texto en
particular, cualquier editor con el que te sientas comode es perfecto.
Si no usas un editor de texto, no sabés cuál elegir o te gustaría empezar
a utilizar otro, aquí te dejamos una lista de los editores de texto más
usualmente utilizados:

- [nano](https://www.nano-editor.org/)
- [vim](https://www.vim.org/) o [Neovim](https://neovim.io/)
- [Geany](https://www.geany.org/)
- [Kate](https://kate-editor.org/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Notepad++](https://notepad-plus-plus.org/)
- [Sublime](https://www.sublimetext.com/)\*
- [Atom](https://atom.io/)\*

Los editores marcados con un asterisco no se encuentran disponibles bajo
licencias de Software Libre, sino bajo licencias privativas.

### Crearse una cuenta de GitHub

Por último es necesario que crees una cuenta en [Github](https://github.com) si
no tienes una. Puedes crear tu cuenta en Github de forma gratuita requiriendo
únicamente ingresar una cuenta de correo electrónico. Por favor, revisa qué
información de tu perfil quieres hacer pública. Aquí te dejo un [instructivo
sobre cómo mantener la dirección de correo electrónico
privada](https://docs.github.com/en/github/setting-up-and-managing-your-github-user-account/managing-email-preferences/setting-your-commit-email-address)
si lo deseas.
