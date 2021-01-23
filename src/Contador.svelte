<script>
	export let counter = 0;
	import { Button } from "sveltestrap";

	function clicou() {
		counter += 1;
	}

	$: if (counter > 3) {
		alert("Chegou em 3, reiniciando contagem");
		counter = 0;
	}
</script>

<div class="card">
	<div class="row">
		<div class="col-12">
			<h4>Contador</h4>
			<h5>Demonstrar eventos</h5>
			<h6>Valor: {counter}</h6>
			<button class="btn btn-primary" on:click={clicou}>Incremento</button
			>
			<Button color="primary" outline on:click={clicou}>Incremento</Button>
			{#if counter < 3}
				<h6>A contador é menor que 3</h6>
			{:else}
				<h6>O contador vai reiniciar</h6>
			{/if}
		</div>
	</div>
</div>

<style>
	.card {
		height: 100%;
	}
	h6 {
		margin: 1em;
	}
</style>
