<script>
	export let title = 'Mes playlist';
	let count = 1;
	let nb1 = 10; 
	let nb2 = 5; 

	function handleClick() {
		count = count + 1;
	}
</script>

<h1>{title}</h1>

<button on:click={handleClick}>Incrémenter</button>

<div>{count}</div>

<input bind:value={nb1} /> * <input bind:value={nb2} />
