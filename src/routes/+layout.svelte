<script>
	import { slide } from 'svelte/transition';
	import '../app.css';
	let { children } = $props();
	let mobileMenuOpen = $state(false);
</script>

<div class="flex flex-col min-h-screen">
	<nav class="sticky flex justify-between items-center px-6 py-4 bg-secondary-50 text-secondary-600  top-0 z-10 border-b border-primary-800">
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
		<button class="md:hidden text-3xl" onclick={() => mobileMenuOpen = !mobileMenuOpen}>
			☰
		</button>
		{#if mobileMenuOpen}
			<ul class="absolute top-full left-0 w-full z-20 bg-secondary-100 text-secondary-700 md:hidden shadow-lg rounded-b-lg p-4"
				in:slide={{ duration: 250 }}
				out:slide={{ duration: 200 }}>
				<li class="hover:text-secondary-900">Home</li>
				<li class="hover:text-secondary-900">About</li>
				<li class="hover:text-secondary-900">Contact</li>
			</ul>
		{/if}
	</nav>

	<!-- Mobile dropdown menu -->

	{@render children()}

	
	<footer class="mt-auto flex flex-col md:flex-row justify-between items-center px-6 py-4 bg-secondary-100 text-sm text-secondary-600 gap-2">

		
		<span>&copy; 2025 MyBlog</span>
		<div class="flex gap-4">
			<a href="#">Privacy</a>
			<a href="#">Terms</a>
		</div>
	</footer>
</div>
