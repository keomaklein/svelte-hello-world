<script>
	let nomes = [
		{ id: 1, valor: "Keoma" },
		{ id: 2, valor: "Julia" },
		{ id: 3, valor: "Maria" },
		{ id: 4, valor: "Jose" },
	];
</script>

<div class="card">
	<div class="row">
		<div class="col-12">
			<h4>Lista</h4>
			<h5>Demonstrar EACH</h5>
			{#each nomes as nome}
				<li>{nome.id} - {nome.valor}</li>
			{/each}
		</div>
	</div>
</div>

<style>
	.card {
		height: 100%;
	}
</style>
