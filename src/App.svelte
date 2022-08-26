<script>
	import '../node_modules/materialize-css/dist/css/materialize.min.css';
	import '../node_modules/materialize-css/dist/js/materialize.min.js';
	import { Router, Link, Route } from "svelte-routing";
	import Navbar from './layout/Navbar.svelte';

import Home from './pages/Home.svelte';
import About from './pages/About.svelte'; 

</script>

<Router>
	<Navbar/>
		<div class="container">
			<Route path="/" component="{Home}" />
			<Route path="about" component="{About}" />
		</div>
</Router>

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