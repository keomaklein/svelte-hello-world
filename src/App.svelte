<script>
	import Title from './Title.svelte';
	import Body from './Body.svelte';
	
	export let name;
	let counter = 0;

	function clicou() {
		counter += 1;
	}

	$: if (counter > 3) {
		alert("Chegou em 3, reiniciando contagem");
		counter = 0;
	}
</script>

<main>
	<Title/>	
	<h1>Hello {name}!</h1>
	<h2>Contador simples: {counter}</h2>
	<button on:click={clicou}>Incremento</button>
	<Body/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>