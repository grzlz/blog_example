<script>
	import '../app.css';
	let { children } = $props();
	let mobileMenuOpen = $state(false);
</script>

<div class="flex flex-col min-h-screen">
	<nav class="flex justify-between items-center px-6 py-4 bg-secondary-50 text-secondary-400 sticky top-0 z-50">
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
		<button class="md:hidden" onclick={() => mobileMenuOpen = !mobileMenuOpen}>
			☰
		</button>
	</nav>

	<!-- Mobile dropdown menu -->
	{#if mobileMenuOpen}
		<ul class="flex flex-col gap-2 px-6 py-4 bg-secondary-100 text-secondary-600 md:hidden">
			<li class="hover:text-secondary-800">Home</li>
			<li class="hover:text-secondary-800">About</li>
			<li class="hover:text-secondary-800">Contact</li>
		</ul>
	{/if}

	{@render children()}

	<footer class="mt-auto flex flex-col md:flex-row justify-between items-center px-6 py-4 bg-secondary-100 text-sm text-secondary-600 gap-2">
		<span>&copy; 2025 MyBlog</span>
		<div class="flex gap-4">
			<a href="#">Privacy</a>
			<a href="#">Terms</a>
		</div>
	</footer>
</div>
