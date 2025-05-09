<script> 
    let nome,cognome,eta,residenza;
    let confermato=false;
</script>


<h1>Input</h1>
nome <input bind:value={nome}>
cognome <input bind:value={cognome}>
eta <input bind:value={eta}>
residenza <input bind:value={residenza}>
<br> <br>
confermato <input type="checkbox" bind:checked={confermato}>
<br> <br>
io sono {nome} {cognome} ed ho {eta} anni e abito a {residenza}
<br><br>
<button disabled={!confermato}>Invia</button>
