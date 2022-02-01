<script>
	import Nav from '../components/Nav.svelte';
	import {QueryClient, QueryClientProvider} from "@sveltestack/svelte-query";

	export let segment;

	const queryClient = new QueryClient({ })
</script>

<style>
	main {
		position: relative;
		max-width: 56em;
		background-color: white;
		padding: 2em;
		margin: 0 auto;
		box-sizing: border-box;
	}
</style>

<Nav {segment}/>

<main>
	<QueryClientProvider client={queryClient}>
		<slot></slot>
	</QueryClientProvider>
</main>
