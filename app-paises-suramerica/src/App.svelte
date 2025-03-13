<script>
  import Paises from "./lib/paises.svelte"; // Importa el componente Paises.
  
  // Lista de países que se utilizarán para generar los componentes.
  const lista = ["colombia", "venezuela", "ecuador", "peru", "brasil"];
</script>

<!-- Contenedor principal -->
<div class="main">
  <!-- Recorre la lista de países -->
  {#each lista as pais}
    <div>
      <!-- Renderiza el componente Paises con cada país de la lista -->
      <Paises {pais} />
    </div>
  {:else}
    <!-- Mensaje mostrado si la lista está vacía -->
    <p>No existen elementos</p>
  {/each}
</div>

<!-- Encabezado de la página -->
<svelte:head>
  <title>Paises de suramerica</title>
</svelte:head>

<style>
  .main {
    display: grid; /* Uso de CSS Grid para el diseño */
    grid-template-columns: repeat(2, 1fr); /* Dos columnas con fracciones iguales */
    grid-gap: 10px; /* Espaciado entre elementos */
    grid-auto-rows: minmax(100px, auto); /* Altura mínima de las filas, ajustable automáticamente */
  }
</style>
