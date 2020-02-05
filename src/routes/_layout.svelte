<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style>
	.layout {
		display: flex;
		align-items: stretch;
		height: 100%;
	}
	main {
		flex: 1 1 auto;
		max-width: 640px;
		width: 100%;
		margin: 0 auto;
		padding: 2rem;
	}
</style>

<div class="layout">
	<Nav {segment}/>
	<main>
		<slot></slot>
	</main>
</div>