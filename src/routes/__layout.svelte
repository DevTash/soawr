<script>
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>

<Header />

<main>
	<slot />
</main>
<!-- 
<footer>
</footer> -->

<style>
	main {
		width: 100%;
		box-sizing: border-box;
	}

	footer {
		min-width: 100vw;
		min-height: 50px;
		background: #e34612;
	}

</style>
