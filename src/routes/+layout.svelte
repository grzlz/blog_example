<script>
	import { slide } from 'svelte/transition';
	import '../app.css';
	let { children } = $props();
	let mobileMenuOpen = $state(false);

	let links = [
		{ text: 'Seguridad', href: '#' },
		{ text: 'Economía', href: '#' },
		{ text: 'Política', href: '#' },
		{ text: 'Cultura', href: '#' },
		{ text: 'Justicia y derechos humanos', href: '#' }
	] 
</script>

<div class="flex flex-col min-h-screen">
	<nav class="sticky flex justify-between items-center px-6 py-4 bg-secondary-50 text-secondary-600  top-0 z-10 ">
		<div class="h-14 w-14 mr-3">
			<img
				src="/logo.png"
				alt="Surcos Logo"
			/>
		</div>

		<ul class="hidden md:flex gap-4">
			<li class="hover:text-secondary-800">Home</li>
			<li class="hover:text-secondary-800">About</li>
			<li class="hover:text-secondary-800">Contact</li>
		</ul>
		<button class="md:hidden text-secondary-700 hover:text-secondary-900" onclick={() => mobileMenuOpen = !mobileMenuOpen} aria-label="Hamburger">
			<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" class="h-7 w-7 transition-transform duration-150 will-change-transform" class:rotate-90={mobileMenuOpen} >
				<line x1="4" y1="6" x2="20" y2="6" />
				<line x1="4" y1="12" x2="20" y2="12" />
				<line x1="4" y1="18" x2="20" y2="18" />
			</svg>
		</button>
	</nav>
		{#if mobileMenuOpen}
		<ul class="flex flex-col bg-secondary-100 font-primary text-secondary-700 md:hidden shadow-lg rounded-b-lg p-4 space-y-3"
			in:slide={{ duration: 400 }}
			out:slide={{ duration: 400 }}>

			{#each links as link}
				<li>
					<a href={link.href} class="flex items-center justify-between gap-3 p-2 rounded-md hover:text-secondary-900 hover:bg-secondary-200 transition">
						<span class="pt-0.5">{link.text}</span>
						<img src="/logo.png" alt={link.text} class="h-5 w-5" />
					</a>
				</li>
			{/each}
		</ul>
		{/if}

	<!-- Mobile dropdown menu -->

	{@render children()}

	<footer class="mt-auto flex flex-col md:flex-row flex-wrap justify-around items-center px-6 py-4 bg-secondary-100 text-sm text-secondary-600 gap-2">

		<span>&copy; 2025 MyBlog</span>
		<div class="flex gap-4">
			<a href="#">Privacy</a>
			<a href="#">Terms</a>
		</div>
	</footer>
</div>
