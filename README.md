* Nombre: Matias Casiba
* Link Github Repo: https://github.com/MatiCasiba/camping-la-cumbre
* Link Netlify: https://camping-la-cumbre.netlify.app/

# Camping la Cumbre
Esta página tratará sobre quienes son "Camping La Cumbre" (que ofrecen, metodos de pago, ubicación, etc). Te mostraré como lo fui armando:
```sh
<header class="encabezado"> # encabezado de la página
  <img src="ubicación de la imagen" alt="nombre de la imagen">
  <p class="texto-nav"><a href="">Texto rodeado con elemento de anclaje</a></p> # la clase me servirá para despues ajustarlo en css sacandole su margen de arriba
</header>

<main> # contenido
  <h1>Titulo</h1>

  <h2>Subtitulo</h2>
  <ul> # listas desordenadas 
    <li><strong>Duchas con agua caliente</strong></li> # Strong lo usaré para destacar el texto y que el navegador le de importancia
    <li>Parrillas</li>
    <li>Enchufes
    </li>
  </ul>

  <h2>Subtitulo</h2>
  <p>texto</p>
  <ul> # algunas listas tendrán un elemento de anclaje
    <li><a href="">Cabañas</a></li>
    <li><a href="">Carpas</a> (¡Nuevo!)</li>
    <li><a href="">Bicicletas</a></li>
    <li>Kayaks (próximamente)</li>
  </ul>

  <h2>Subtitulo</h2>
  <p><b>Texto</b></p> # A diferencia del elemento strong, el elemneto b lo utilizo solo por decoración para destacar el texto
  <ul>
    <li><a href="" target="_blank">La Nación</a></li> # target="_blank" será para que el usuario al momento de seleccionarlo, se abra otra pestaña sin que cambie la nuestra.
    <li><a href="" target="_blank">Página 12</a></li>
  </ul>

  <h2>Subtitulo</h2>
  <ol> # ol son listas ordenadas, unas de su lista tendrá identada listas desordenadas (ul>li)
    <li>Texto:
      <ul>
        <li>Almacén.</li>
        <li>Duchas calientes.</li>
        <li>Guardia de enfermería.</li>
        <li>Vigilancia brindada por <a href="">Prosegur</a>.</li>
        <li>Energía eléctrica.</li>
        <li>Asistencia a nuestros huéspedes.</li>
      </ul>
    </li>
    <li><b>Texto.</b></li>
  </ol>
</main>

<footer>Copyright 2024</footer> # pie de página
```
* En el archivo style.css eh tocado hecho unos ajustes al comienzo:
```sh
*{
  box-sizing: border-box; # permite que el navegador defina el tamaño del elemento
}

img{
  width: 100%; # hará que la imagen ocupe el ancho total de la pantalla, lo que logra es que cuando achique la pantalla, se va achicando la imagen
}

footer{ # ell pie de la página tendrá un color de fondo negro, con un alto de 100px y el texto en el centro
  background-color: #111;
  height: 100px;
  text-align: center;
}

.encabezado{ # clase que contiene el elemento header
  font-size: 20px;
}
.texto-nav{ # clase que contiene el elemento p dentro del header
  margin-top: 0; # elimino el espacio que tiene arriba, con la finalidad de que lo que haya en el elemento p, quede cerca de la imagen
}
```

## Color y fuente
Le agruegé colores y fuente a la página, estos son los colores trabajados:
```sh
:root{
  --colorFondo: #faf4ea; # cremita
  --colorEnlace: #ed862b; # naranaja
  --colorTitulo: #6c3f26; # marrón oscuro
  --colorFondoSubtitulos: #614433; # marrón no tan oscuro
  --colorLetraSubtitulo: #ebb912; # amarillo
  --colorEnlace1: #10abfe; # celeste
  --colorEnlace2: #ff4b3e; # rojo
}
```
* :root me va a permitir majerar el nodo principal del documento, creo los colores acá y los voy a usar luego de esta forma: 
```sh
body{
  background-color: var(--colorFondo);
}

.color-sub-unico{
  color: var(--colorLetraSubtitulo);
}
```
No todo el tiempo usaré var(), bien podrás verlo al momento de dar colores en letras de algunos elementos o fondo:
```sh
h2{
  color: #faf4ea;
}
p{
  color: #614433;
}
ul>li , ol>li{ # le da el mismo color a las listas desordenadas y ordenadas
  color: #614433;
}
footer{
  background-color: #111; # negro
}
```

### Clases
Para dar diseños únicos y no sean hereditarios de algunos elementos, eh creado clases, se las asigné a algunos elementos del archivo index.html, estas son las clases trabajadas en el archivo style.css:
```sh
.encabezado p{
  font-size: 20px; # tamaño del texto para los elementos p que contenga el header
}
.encabezado a{
  font-weight: bold; # grosor del texto para los elementos de anclaje que contenga el elemento header
}
.color-sub-unico{
  color: var(--colorLetraSubtitulo); # color del texto para un elemento h2 con esta clase
}
.color-ln{
  color: var(--colorEnlace1); # color para un elemento a
}
.color-p12{
  color: var(--colorEnlace2); # otro color para un elemento a
}
```

### Fuente
Agregué una fuente para el elemento body, de esta forma será hereditario para todos los elementos que se enecuentren dentro de este:
```sh
body{
  font-family: Verdana, Arial, sans-serif;
}
```

## Actualización
Eh modificado una cosa en footer, agregue un color a la letra en amarillo y lo centre al texto de manera vertical tambien:

```sh
footer{
  background-color: #111;
  height: 100px;
  line-height: 100px; # igual al alto del footer para centrar verticalmente
  text-align: center;
  color: #ebb912;
}
```

