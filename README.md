Evidencia práctica teórica 3er trimestre

Introducción:

Este documento describe la funcionalidad del código HTML y JavaScript proporcionado para una aplicación de consulta de asesoría energética. La aplicación permite a los usuarios buscar y visualizar datos relacionados con asesoría energética a través de una interfaz web.

1. Estructura del Código HTML:

El código HTML proporciona la estructura básica de la página web. Contiene los siguientes elementos:

- Encabezado (`<head>`): Define metadatos como la codificación de caracteres, la escala inicial de la vista y el título de la página.
  
- Cuerpo (`<body>`): Contiene los elementos visibles de la página, incluyendo un contenedor principal con el título de la aplicación y un formulario de búsqueda. Además, hay un botón para realizar la búsqueda y una lista (`<ul>`) donde se mostrarán los resultados de la consulta.

2. Funciones JavaScript:

El código JavaScript proporciona la funcionalidad dinámica de la aplicación. Contiene las siguientes funciones:

- `fetchData()`: Esta función realiza una solicitud HTTP para obtener los datos de asesoría energética de una API remota. Una vez que se reciben los datos en formato JSON, llama a la función `displayData()` para mostrarlos en la página.

- `displayData(data)`: Esta función recibe los datos obtenidos de la API y los muestra en la página web. Crea elementos de lista (`<li>`) para cada conjunto de datos y los agrega a la lista (`<ul>`).

- **`filterData()`:** Esta función se activa cada vez que el usuario ingresa un valor en el campo de búsqueda. Filtra los datos mostrados en la página según el valor ingresado. Compara el valor de búsqueda con los nombres, CIF, comercializadoras y estados de los elementos de datos y muestra solo aquellos que coinciden.

- `displayFilteredData(filteredData)`: Esta función recibe los datos filtrados y los muestra en la página web. Limpia cualquier contenido previo en la lista de datos y agrega solo los elementos filtrados.

- `search()`: Esta función se activa cuando el usuario hace clic en el botón "Lista". Llama a la función `fetchData()` para obtener los datos de la API y actualizar la lista de datos en la página.

Problemas de funcionalidad:

Los problemas que he tenido con esta pagina es en el boton de buscar, que no cumplia su funcionalidad con exactitud, ya que al darte, en vez de realizar una nueva busqueda, reseteaba al inicio de las listas, en el que podias buscar desde 0 otra vez, la solucion que se ha implementado en este caso, es cambiar el nombre del boton a "listas", para especificar su funcionalidad
