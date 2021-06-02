<!-- .slide: class="slide-title" -->

# Introducción a Git y Github

## [Santiago Soler](https://santisoler.github.io)<sup>1,2</sup> y [Mariana Gomez](https://github.com/MGomezN)<sup>3</sup>

<sup>1</sup>[*CONICET, Argentina*](https://www.conicet.gov.ar/)
<br>
<sup>2</sup>[*Instituto Geofísico y Sismológico Volponi, UNSJ, Argentina*](http://igsv.unsj.edu.ar/)
<br>
<sup>3</sup>*Centro de Investigación Científica y de Educación Superior de Ensenada, Baja California (CICESE), México*

<div class="logo">
<a href="https://geolatinas.weebly.com/">
<img src="images/logos/geolatinas-logo-overlay.png" style="max-width: 200px;">
</a>
</div>

---

# Información

- **Cuándo:** [Sábado 5 de Junio 2021 de 15:00 a 19:00 GMT](https://www.timeanddate.com/worldclock/fixedtime.html?msg=Introducci%C3%B3n+a+Git+%7C+Geolatinas&iso=20210605T12&p1=51&ah=5)
- **Notas colaborativas:** Etherpad: https://pad.disroot.org/p/2o7i0afvxpe8jcdy
- **Material:**  https://swcarpentry.github.io/git-novice-es

---

# Requisitos

1. Terminal
2. Instalar git
3. Editor de texto
4. Cuenta en GitHub
5. Llenar formulario de registro al taller

No es necesario tener experiencia en el uso de la terminal.

---

# Objetivos

- Gestionar versiones con git
- Aplicar las mejores prácticas de git
- Trabajar con repositorios remotos (GitHub)
- Trabajar de forma colaborativa

---

# Contenidos

<div class="container">
<div class="column">

- Control Automatizado de Versiones
- Configurando Git
- Creando un repositorio
- Rastreando Cambios
- Explorando el "History"

</div>
<div class="column">

- Ignorando cosas
- Repositorios remotos en GitHub
- Trabajos en colaboración
- Conflictos

</div>
</div>

---

# Control Automatizado de Versiones

---

<img src="images/phdcomics.png" alt="" style="height: 90vh">

<div class="bottom">
<a href="http://phdcomics.com/comics/archive.php?comicid=1531">
"Piled Higher and Deeper" by Jorge Cham
</a>
</div>

---

# Sistema de control de versiones

<img src="images/play-changes.svg" alt="" style="height: 85vh">

---

# Sistema de control de versiones

<img src="images/versions.svg" alt="" style="height: 85vh">

---

# Sistema de control de versiones

<img src="images/merge.svg" alt="" style="height: 85vh">

---

# Sistema de control de versiones

- Realiza seguimiento de cambios o **commits**
- Es como un _deshacer_ sin límites.
- Permite que mucha gente trabaje en lo mismo en paralelo.
- **Repositorio:** El historial completo de **commits**


---

Imagina que has redactado un excelente párrafo para un artículo que estás
escribiendo, pero más tarde lo estropeas.

¿Cómo recuperarías aquella excelente versión de la conclusión? ¿Es esto
posible?

---

# Configurando git

---

# Configurando git

- Nombre
- Mail
- Editor de texto favorito

---

# Creando un repositorio

---

## Comandos útiles de bash

- `mkdir`: crea una nueva carpeta (_make directory_)
- `ls`: lista los archivos y carpetas del directorio actual (_list_)
- `cd`: cambia de directorio (_change directory_)

---

## Comandos de git

- `git init`: Crea un nuevo repositorio en la carpeta actual
- `git status`: Revisamos el estado del repositorio

---

# Rastreando Cambios

---

## Staging Area

<img src="images/git-staging-area.svg" alt="" style="height: 85vh">

---

## Comandos de git

- `git add`: Añade uno o más archivos al **staging area**
- `git commit`: Registra los cambios de la **staging area** en un commit
- `git log`: Muestra un historial de cambios
- `git diff`: Muestras las diferencias entre el estado actual de los archivos
    y la versión del commit más reciente
- `git diff --staged`: Muestra las diferencias entre el estado de los archivos
    en el staging area y la versión del commit más reciente.

---

## Ejercicios

---

## 1. Multiple choice

---

## 2. Haciendo Commit a Multiples Archivos

1. Agrega algún texto a `mars.txt` anotando tu decisión de considerar Venus como base.
1. Crea un nuevo archivo `venus.txt` con tus pensamientos iniciales acerca de
   Venus como base para tí y tus amigxs.
1. Agrega los cambios de ambos archivos al **staging area**, y haz un **commit** de esos cambios.


---

## 3. Repositorio bio

1. Crea un nuevo repositorio Git en tu computadora, llamado `bio`.
1. Escribe una autobiografía de tres líneas en un archivo llamado `me.txt`, haz
   **commit** de tus cambios.
1. Modifica una línea, agrega una cuarta línea.
1. Muestra las diferencias entre el estado actualizado y el original.


---

# Explorando el historial

---

<img src="images/git-checkout.svg" alt="" style="height: 85vh">

---

## Comandos de git

- `HEAD` simboliza el commit más reciente
- `git diff HEAD~2 main` nos muestra las diferencias entre main y los últimos
    dos commits.
- `git show HEAD~1` nos muestra los cambios realizados por el penúltimo commit.
- Podemos usar el identificador del commit en vez de `HEAD`.
- `git checkout` nos deja _visitar_ commits anteriores.
- Nunca hay que hacer commits si no estamos en `HEAD`.

---

# Do you want columns?

<div class="container">

<div class="column">
<img src="images/about.jpg" style="margin-top: 5%; border-radius: 50%; width: 80%;">
</div>

<div class="col-2">
<div class="centered">

* Licenciado en Física (UNR)
* Estudiante de Doctorado en Geofísica (UNSJ)
* Becario Doctoral de CONICET
* Desarrollador de [Fatiando a Terra](https://www.fatiando.org)
* Miembro de [Computer-Oriented Geoscience Lab](https://www.compgeolab.org)

</div>
</div>

</div>

---

# You can add fade-in animations

<div class="container">

<div class="column fragment fade-in">

First element

</div>

<div class="column fragment fade-in">

Second element

</div>

</div>

---

## Even on lists

<ul>
<li class="fragment fade-in">First element</li>
<li class="fragment fade-in">Second element</li>
<li class="fragment fade-in">Third element</li>
</ul>

---

## Highlight current item on list

<ol>
<li class="fragment highlight-current-blue">First element</li>
<li class="fragment highlight-current-blue">Second element</li>
<li class="fragment highlight-current-blue">Third element</li>
</ol>

---

# You can put footnotes

<div class="bottom">

https://www.blog.pythonlibrary.org/2019/04/11/python-used-to-take-photo-of-black-hole/

</div>

---

<!-- .slide: data-background-color="#FAFAFA" -->

## You can change the background color

---

## Add quotes

<blockquote>
This is a quote
</blockquote>

---

# Contacto

<div>

<ul class="fa-ul" style="">
<li><i class="fa-li fa fa-envelope"></i>

[santiago.r.soler@gmail.com](mailto:santiago.r.soler@gmail.com)

</li>
<li><i class="fa-li fab fa-twitter"></i>

[@santirsoler](https://twitter.com/santirsoler)

</li>
<li><i class="fa-li fa fa-globe-americas"></i>

[santisoler.github.io](https://santisoler.github.io)

</li>
</ul>

</div>

---

<!-- .slide: class="slide-license" -->

<p class="license-icons">
<i class="fab fa-creative-commons"></i><i class="fab fa-creative-commons-by"></i>
</p>

El contenido de esta presentación está disponible bajo

[Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/)

---

<!-- .slide: class="slide-title" -->

# Muchas gracias
