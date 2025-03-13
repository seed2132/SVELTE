<script>
  //importamos el componente parimpar.svelte y lo llamamos parimpar
  import ParImpar from './lib/parImpar.svelte';
  let valor=0;

  // escuchamos el evento input
  const listenInput = (event) => valor = event.target.value
</script>



<main>
  
  <ParImpar numero={valor}/>
  <input value={valor} on:input={listenInput}>

</main>