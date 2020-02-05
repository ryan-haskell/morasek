<script>
	export let segment;
</script>

<style>
	aside {
		min-width: 300px;
		background: linear-gradient(#ab655e, #ab655e);
		color: white;
		box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.5);
		border-right: 1px solid rgb(160, 120, 120);
	}
	nav {
		display: flex;
		height: 100%;
		align-items: center;
		justify-content: center;
	}
	ul {
		margin: 0;
		padding: 0;
		list-style: none;
	}
	li {
		display: block;
		margin-bottom: 1rem;
	}
	a {
		font-size: 2rem;
		text-align: center;
	}
</style>

<aside>
	<nav>
		<ul>
			<li><a class:selected='{segment === undefined}' href='.'>home</a></li>
			<li><a class:selected='{segment === "about"}' href='about'>about</a></li>

			<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
					the blog data when we hover over the link or tap it on a touchscreen -->
			<li><a rel=prefetch class:selected='{segment === "thots"}' href='thots'>thots</a></li>
		</ul>
	</nav>
</aside>