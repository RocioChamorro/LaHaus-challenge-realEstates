# Prueba Técnica - Front End Software Engineer - La Haus

Las **caraterísticas técnicas** requeridas:
- Cargar una lista de colecciones de real estates desde el [API real-estates](https://lh-real-estates-challenge-api.herokuapp.com/real-estates)
- Listar las colecciones de real estates.
- Hacer la maquetación responsive según el [Figma Prueba-Técnica](https://www.figma.com/file/sW5Z8Y3pHim5OYIAAvRtd9/Prueba-Técnica?node-id=1%3A2).
- Usar únicamente las clases CSS que proporciona TailwindCSS.
- Si se va a usar CSS personalizado justificar en un comentario por qué se necesita o extender TailwindCSS.
- La card que dice "Crea una nueva lista" no debe hacer nada, solo hace parte de la maquetación.

Otros **Requerimiento**:
- Crear repositorio en Github, agregar como colaboradores a los usuarios pastuxso y DixonMedina en caso de que el repositorio sea privado, esto con el fin de echarle una mirada a tu progreso y entender cual es tu flujo de trabajo usando git.
- Usar VueJS 2 .
- Usar NuxtJS.
- Usar TailwindCSS.
- Hacer deploy y enviar la url pública (puedes usar Heroku o cualquier otro de tu preferencia).

## Desarrollo Front-end 

### A nivel de planificación

* Inicialmente revisé de manera general todos los recursos solicitados y brindados para comprender y fijar mis objetivos diarios.

* Adquirí los conocimientos necesarios mediante las documentaciones oficiales y tutoriales descritas en "Recursos de autoaprendizaje" de una manera global empezando por NuxtJS para iniciar y luego de forma específica aprendiendo VueJs y tailwindcss para culminar con el proyecto.

* **Prioricé** realizar checked de productos mínimos viables de mis avances



### A nivel del desarrollo 

#### Arquitectura de la aplicación

Con NuxtJS obtuve una estructura de directorios predeterminada la cual fui agregando otros directorios como assets y otros componentes  reutilizables según la necesidad.

La vista de "Lista de favoritos" del reto técnico, consideré crearla en un archivo secundario dentro del directorio `Pages` a fin de que el proyecto puede ser escalable y tener diversas vistas por ello agregué una vista general de "Bienvenido" como componente del archivo principal index.vue.

#### Diseño responsivo

Utilicé el diseño de Caja Flexible, comúnmente conocido como ​ `Flexbox` permitiendome crear un diseño adaptativo para **mobile y desktop**

#### A nivel de datos

Para consumir la API de real-estates decidí usar `Axios` ya que tiene una sencilla integración con Vue y la API Fetch es muy potente pero no es totalmente soportada.

#### Deploy

                               https://mysterious-everglades-83608.herokuapp.com/favoritesList
***


### Recursos de autoaprendizaje:

* [Vue.js](https://es.vuejs.org/)
* [NuxtJS](https://nuxtjs.org/)
* [Nuxt js: aplicaciones universales con vue js - udemy](https://www.udemy.com/course/nuxt-js-aplicaciones-universales-con-vue-js/)
* [tailwindcss](https://tailwindcss.com/)
* [tailwindcss - Bluuweb](https://www.youtube.com/watch?v=97hHnlnxpPQ&list=RDCMUCH7IANkyEcsVW_y1IlpkamQ&start_radio=1&rv=97hHnlnxpPQ&t=552)


***
