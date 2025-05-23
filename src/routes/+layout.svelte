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
			<!-- Desktop menu -->
			<ul class="hidden md:flex gap-4">
				<li class="hover:text-secondary-800">Home</li>
				<li class="hover:text-secondary-800">About</li>
				<li class="hover:text-secondary-800">Contact</li>
			</ul>

			<!-- Mobile menu button -->
			<button class="md:hidden text-3xl hover:text-secondary-700" onclick={() => mobileMenuOpen = !mobileMenuOpen}>
				☰
			</button>
		</nav>
		{#if mobileMenuOpen}
		<ul class="flex flex-col bg-secondary-100 font-primary text-secondary-700 md:hidden shadow-lg rounded-b-lg p-4 space-y-3"
			in:slide={{ duration: 250 }}
			out:slide={{ duration: 300 }}>

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
