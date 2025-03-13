<script>
  let listdata=[];
  let loading;
  fetch("https://jsonplaceholder.typicode.com/users")
  .then((response)=>response.json())
  //.then((results)=>listdata=results)
  .then(results=>{
  listdata=results
  console.log(listdata)
  loading=false
  })
  </script>

  <table class="table table-striped table-hover">
  <thead>
  <tr id="encabezado">
  <th>#</th>
  <th>Nombre</th>
  <th>Usuario</th>
  <th>Ciudad</th>
  <th>Email</th>
  </tr>
  </thead>
  <tbody>
    {#each listdata as values}
    <tr>
    <td>{values.id} </td>
    <td>{values.name}</td>
    <td>{values.username}</td>
    <td>{values.address.city}</td>
    <td>{values.email}</td>
    </tr>
    {/each}
    </tbody>
    </table>
    <style>
    #encabezado{
    color:darkblue;
    background-color: rgb(23, 233, 93);
    } 
    </style>