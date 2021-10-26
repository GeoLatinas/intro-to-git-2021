<!-- .slide: class="slide-title" -->

# Introducción a Git y Github

## [Agustina Pesce](https://aguspesce.github.io)<sup>1,2</sup> y [Mariana Gomez](https://github.com/MGomezN)<sup>3</sup>

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

- **Cuándo:** [Sábado 4 de Diciembre 2021 de 15:00 a 19:00 GMT](https://www.timeanddate.com/worldclock/fixedtime.html?msg=Introduccion+a+Git&iso=20211204T12&p1=1078&ah=4)
- **Notas colaborativas:** Etherpad: https://pad.disroot.org/p/2o7i0afvxpe8jcdy
- **Material:**  https://swcarpentry.github.io/git-novice-es
- **Diapositivas:**  https://geolatinas.github.io/intro-to-git-2021

---

# Requisitos

1. Terminal
2. Instalar git
3. Editor de texto
4. Tener una cuenta en GitHub
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
- Configuración Git
- Cómo crear un repositorio
- Cómo registrar los cambios
- Explorar el "History"

</div>
<div class="column">

- Cómo ignorar cosas
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

¡Vamos a configurarlo juntos!

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

¡Vamos a crear un repositorio juntos!

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

¡Vamos hacer un commit!

---

## Ejercicios

---

## 1. Multiple choice

¿Cuál de los siguientes mensajes de commit sería el más apropiado para el último commit hecho a mars.txt?

1. “Changes”
2. “Added line ‘But the Mummy will appreciate the lack of humidity’ to mars.txt”
3. “Discuss effects of Mars’ climate on the Mummy”

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

## Ejercicios

---

## 1. Multiple choice

Jennifer ha realizado cambios en el script en el que ha estado trabajando durante semanas, y las modificaciones que hizo esta mañana “corrompieron” el script y ya no funciona.
Por suerte, ha estado usando Git...

---

## 1. Multiple choice

¿Cuáles comandos le permitirán recuperar la última versión estable de su script llamado script.py?

<ol>
    <li>
    <pre><code>$ git checkout HEAD
    </code></pre>
    </li>
    <li>
    <pre><code>$ git checkout HEAD script.py
    </code></pre>
    </li>
    <li>
    <pre><code>$ git checkout HEAD~1 script.py
    </code></pre>
    </li>
    <li>
    <pre><code>$ git checkout [ID_last_commit] script.py
    </code></pre>
    </li>
    <li>
    <pre><code>Ambos 2 y 4
    </code></pre>
    </li>
</ol>

---

¿Cuál es el output de `cat venus.txt` al final de este conjunto de comandos?

```bash
cd planets
nano venus.txt # agrega el siguiente texto: Venus is beautiful and full of love
git add venus.txt
nano venus.txt # agrega el siguiente texto: Venus is too hot to be suitable as a base
git commit -m "Comment on Venus as an unsuitable base"
git checkout HEAD venus.txt
cat venus.txt #esto imprimirá el contenido de venus.txt en la pantalla
```

<ol>
    <li>
    <pre><code>Venus is too hot to be suitable as a base
    </code></pre>
    </li>
    <li>
    <pre><code>Venus is beautiful and full of love
    </code></pre>
    </li>
    <li>
    <pre><code>Venus is beautiful and full of love
Venus is too hot to be suitable as a base
    </code></pre>
    </li>
    <li>
    <pre><code>Error because you have changed venus.txt without committing the changes
    </code></pre>
    </li>
</ol>

---

## 2. Deshacer cambios añadidos al stage area

- `git checkout` puede usarse para restaurar un commit anterior cuando cambios
  no marcados se han hecho, pero ¿También funcionará para los cambios que se
  han marcado pero no se han vuelto commit?

- Haz un cambio a `mars.txt`, agrega el cambio y usa `git checkout` para ver si
  puedes eliminar tu cambio.

---

# Ignorando cosas

¿Qué pasa si tenemos archivos que no queremos que Git rastree?


Debemos crear un **.gitignore**

---

Probemoslo...

---

# Repositorios remotos en GitHub

---

<img src="images/github.svg" alt="" style="width: 40%;">

- Nos permite almacenar repositorios "en la nube"
- Facilita la colaboración
- Issues y PullRequests
- Mucho más:
    - Code review
    - Releases
    - Continuous Integration
    - GitHub Pages

---

# Crear un repositorio en GitHub

<div class="r-stack">
<img class="fragment current-visible" src="images/github-create-repo-01.png" alt="" style="width: 50%">
<img class="fragment current-visible" src="images/github-create-repo-02.png" alt="" style="width: 50%">
</div>

---

# Subir cambios a GitHub

¿Cómo se ve el reposotorio local y el remoto?

<img class="fragment current-visible" src="images/git-freshly-made-github-repo.svg" alt="" style="width: 50%">

---

# Subir cambios a GitHub

Pero lo que quiero hacer es: 

<img class="fragment current-visible" src="images/github-repo-after-first-push.svg" alt="" style="width: 50%">

---

## Comandos de git

- `git remote add origin URL`: Agrega la dirección de repositorio de GitHub bajo el nombre `origin`.
- `git remote -v`: Verifica que esté bien configurado.    
- `git push origin main`: Sube los cambios al repositorio de GitHub.

---

Probemoslo...

---

# Trabajos en colaboración

---

# Trabajos en colaboración

<img class="fragment current-visible" src="images/github-repo-setting.png" alt="" style="width: 50%">
</div>

---

## Comandos de Git

- `git clone [url]` clona un repositorio contenido en GutHub.
- `git push origin main` envia los cambios hacia el repositorio de GitHub.
- `git pull` descargar los cambios hechos por el colaborador desde GitHub.

---

## Un flujo de trabajo colaborativo básico

1. Actualizar el repositorio local:
```
git pull origin main
```
1. Realizar los cambios:
```
git add
```
1. Realizar un commit:
```
git commit -m "[mensaje]"
```        
1. Cargar las actualizaciones a GitHub:
```
git push origin main
```

_Es mejor hacer varias actualizaciones pequeñas que un commit grande con cambios enormes._

_Commits pequeños son más fáciles de leer y revisar._

---

# Conflictos

---

¡Hagamos un lio!

---

## Consejos para trabajos colaborativos 


**La resolución de conflictos cuesta tiempo y esfuerzo**,

---

### Algunas técnicas para reducir conflictos:

* Hacer `pull` con mayor frecuencia, especialmente antes de empezar una nueva tarea.
* Hacer comentarios mas cortos y concisos
* Cuando sea apropiado, dividir archivos grandes en varios pequeños de manera que sea menos probable que dos autores alteren el mismo archivo simultáneamente.

---

Los conflictos también **pueden ser minimizados con estrategias de administración de proyectos**:

* Aclarar con tus colaboradores quién es responsable de cada área.
* Discutir con ellos en qué orden deben realizarse las tareas para que no trabajen simultaneamente en las mismas lineas.
* Si los conflictos son de estilo (e.g. tabulaciones vs. espacios), establecer una convención que rija el proyecto y utilizar herramientas de estilo de código.

---

No esperes para usarlo ...

lee 
pregunta 
 y usalo para cualquier proyecto que tengas

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
