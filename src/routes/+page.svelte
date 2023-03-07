<script>
	export let title = 'Mes playlist';
	let count = 1;
	let nb1 = 10;
	let nb2 = 5;
    let result = 0;
	function handleClick() {
		count = count + 1;
	}

	function calculate() {
		 result = nb1 * nb2;
	}
	calculate();

    let fruits = [
        'pomme',
        'poire',
        'orange',
        'banane'
    ];
</script>

<h1>{title}</h1>

<ul>
	{#each fruits as fruit, k}
		<li> {k+1} {fruit}</li>
	{/each}
</ul>

<button on:click={handleClick}>Incrémenter</button>

<div>{count}</div>

<input bind:value={nb1} on:keyup={calculate} /> * <input bind:value={nb2} on:keyup={calculate} /> {result}


{#if count % 2 === 0 }
	<p>Ce nombre est divisible par deux</p>
{:else}
	<p>Ce nombre n'est divisible par deux</p>
{/if}