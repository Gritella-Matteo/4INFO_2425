<script>
    import Counter from "$lib/components/counter.svelte";
    let contator=0
</script>
<h1>Questa è la pagina about!</h1>
<h2>il contatore vale: {contator}</h2>

<Counter bind:counter={contator}/>