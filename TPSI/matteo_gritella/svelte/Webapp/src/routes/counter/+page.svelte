<script>
    import Counter from "$lib/components/counter.svelte";
    import DoubleCounter from "$lib/components/double_counter.svelte";
    let numeri=[1,7,2,6,9,10];
    let contator=0;
    let contator2=0;
    $: doppio=contator*2
</script>
<h1>Pagina Counter</h1>
{#if contator<5}
    <h2 class="rosso">Il valore del 1 contatore vale: {contator}</h2>
{:else}
    <h2 class="verde">Il valore del 1 contatore vale: {contator}</h2>
{/if}
{#if contator2%2==0}
    <h2 class="sottolineato">Il valore del 2 contatore vale: {contator2}</h2>
{:else}
<h2>Il valore del 2 contatore vale: {contator2}</h2>
{/if}


<h2> doppio del primo contatore vale: {doppio}</h2>


<Counter bind:counter={contator}/>
<DoubleCounter bind:counter={contator2}/>

<ul>
    {#each numeri as numero,indice}
        <li>numeri [{indice}]:{numero}</li>
    {/each}
</ul>


<style>
    .rosso{color:red;}
    .verde{color:green;}
    .sottolineato{ text-decoration: underline;}

</style>