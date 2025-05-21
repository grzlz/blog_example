<script>
	import '../app.css';

	let { children } = $props();
</script>

<div class="flex flex-col min-h-screen">
	<nav class="flex justify-between sticky top-0 items-center px-6 py-4 bg-secondary-50 text-secondary-400">
		<div class="text-3xl font-bold text-primary-500">MyBlog</div>
		<ul class="flex gap-4">
			<li class=" hover:text-secondary-800">Home</li>
			<li class="hover:text-secondary-800">About</li>
			<li class=" hover:text-secondary-800">Contact</li>

		</ul>
	</nav>

	
	{@render children()}

    <!-- 🔻 Footer -->
    <footer class="mt-auto flex justify-between items-center px-6 py-4 bg-secondary-100 text-sm text-secondary-600">
        <span>&copy; 2025 MyBlog</span>
        <div class="flex gap-4">
            <a href="#">Privacy</a>
            <a href="#">Terms</a>
        </div>
    </footer>
	
</div>