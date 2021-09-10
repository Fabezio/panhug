<script>
	import { page } from '$app/stores';
	import logo from './svelte-logo.svg';
</script>

<nav>
	<div class="brand">
		<div class="item flex-2">PANHUG	</div>

	</div>
	<ul>
		<!-- <li><div class="item flex-2">PANHUG	</div></li> -->
		<li><div class="item flex-2">Je suis: </div></li>
		<li class:active={$page.path === '/'}><a sveltekit:prefetch href="/">Pansexuel</a></li>
		<li class:active={$page.path === '/about'}><a sveltekit:prefetch href="/about">Panromantique</a></li>
		<li class:active={$page.path === '/todos'}><a sveltekit:prefetch href="/todos">Atypique</a></li>
	</ul>
</nav>


<style>
	nav {
		display: grid ;
		grid-template-columns: auto 1fr;
	}
	.brand {
		align-self: center;
	}
	ul {
		/* border-bottom: 2px solid linear-gradient(left, cyan, magenta, yellow) !important; */
		/* background: 2px solid linear-gradient(left, cyan, magenta, yellow) !important; */
		/* border-bottom: 2px solid cyan; */
		align-self: center;
		display: flex;
		justify-content: flex-start;
		list-style-type: none;
		flex: 1 0 auto;
		/* height: 2rem; */
	}
	.flex-2 {
		flex: 2;
		padding: 0 1em;
	}
	.item, a {
		color: whitesmoke;
		text-transform: uppercase;
		text-shadow: 0 0 7px black;
		
	}
	.item {
		
		/* display: flex;	 */
		
		height: 100%;
		/* align-items: center; */
		/* color: var(--heading-color); */
		font-weight: 700;
		font-size: 1rem;
		letter-spacing: 10%;
		text-decoration: none;
		transition: all 0.2s linear;
	}
	nav a {
		/* display: flex; */
		height: 100%;
		/* align-items: center; */
		padding: 4px 1em;
		/* color: var(--heading-color); */
		font-weight: 600;
		font-size: 1rem;
		/* text-transform: uppercase; */
		letter-spacing: 10%;
		text-decoration: none;
		/* transition: box-shadow 0.1s linear; */
		background: -webkit-linear-gradient(left, 
		/*
		transparent 0%, 
		*/
		
		
		cyan 33%, 
		
		yellow 66%, 
		
		magenta 100%
		);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}
	/* li {
		padding:  auto;
	} */
	
	a:hover {
		
		/*
		box-shadow: 0 0 3px black; 
		*/
		
		/* color: none; */
	}
</style>
