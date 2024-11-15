* Nombre: Matias Casiba
* Link Github Repo:
* Link Netlify:

# Camping El Lago
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