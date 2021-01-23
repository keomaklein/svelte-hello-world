<script>
	import Header from "./Header.svelte";
	import Footer from "./Footer.svelte";
	import Contador from "./Contador.svelte";
	import Lista from "./Lista.svelte";
	export let name;

	import { Col, Row } from "sveltestrap";
</script>

<main>
	<Header />	
	<div class="row">
		<div class="col-12" style="margin:4em">
			<h1>Hello {name}!</h1>
		</div>
	</div>
	<div class="row">
		<div class="col-12 col-xl-6 col-md-6 col-lg-6">
			<Contador />
		</div>
		<div class="col-12 col-xl-6 col-md-6 col-lg-6">
			<Lista />
		</div>
	</div>
	<Footer />
</main>

<style>
	main {
		text-align: center;
		padding: 0;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

</style>
