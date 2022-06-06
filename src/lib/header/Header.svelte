<script>
	import { page } from '$app/stores'
</script>

<header>
	<div class="branding">
		SOAWR
	</div>
	<nav>
		<ul>
			<li><a href="/" class:route-active={$page.url.pathname === '/'}>home</a></li>
			<li><a href="#how-it-works" class:route-active={$page.url.pathname.search('#how-it-works') !== -1}>how it works</a></li>
			<li><a href="#why-us" class:route-active={$page.url.pathname.search('#why-us') !== -1}>why us</a></li>
			<li><a href="/cars" class:route-active={$page.url.pathname === '/cars'}>explore cars</a></li>
			<li><a href="/request-a-car" class:route-active={$page.url.pathname === '/request-a-car'}>request car</a></li>
			<!-- <li><a href="/contact" class:route-active={$page.url.pathname === '/contact-us'}>contact us</a></li> -->
		</ul>
	</nav>
</header>

<style>
	header {
		display: grid;
		grid-auto-flow: column;
		align-items: center;
		justify-content: space-between;

		padding: 2rem 0;
	}

	.branding {
		text-transform: uppercase;
		font-weight: 900;
		font-size: 2rem;
	}

	ul {
		display: grid;
		grid-auto-flow: column;
		column-gap: 2rem;
		justify-content: start;

		list-style: none;
	}

	a {
		text-transform: uppercase;
		padding: 0.5rem;
	}

	a:hover {
		text-decoration: underline;
	}

	.route-active {
		font-weight: 700;
	}
</style>