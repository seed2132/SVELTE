<script>
    export let numero; // exportamos la variable numero para poder llamarla en app.svelte
    let resultado; //variable local
    $: if (numero===0)
        resultado="neutro";
    else 
        if (numero%2===0)
            resultado="par";
    else
            resultado="impar";

</script>
<p>El numero {numero} es {resultado}</p>
<style>
    p{
        color: blue;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 25px;
    }
</style>