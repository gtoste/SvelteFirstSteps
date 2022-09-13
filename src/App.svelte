<script>
	import Tailwindcss from './Tailwindcss.svelte';

	export let name;


	import { Router, Link, Route } from "svelte-routing";
	import Home from "./routes/Home.svelte";
	import About from "./routes/About.svelte";
	import Blog from "./routes/Blog.svelte";
	import Board from './routes/Board.svelte';
	import Api from './routes/Api.svelte';
	import Footer from './components/Footer.svelte';
	import Header from './components/Header.svelte';

	export let url = "";

</script>

<Tailwindcss />

<Header />	
<main>
	
<Router url="{url}">
	  <Route path="blog"><Blog/></Route>
	  <Route path="about"><About/></Route>
	  <Route path="board"><Board/></Route>
	  <Route path="api"><Api/></Route>
	  <Route path="/"><Home /></Route>
</Router>
</main>

<Footer />

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
