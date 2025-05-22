<script>
    import Newspaper from "$lib/Newspaper.svelte";
</script>

<header class="text-center bg-secondary-900 p-6">
	<img src="/header.png" alt="Surcos Logo" class="mx-auto mb-12 w-72 md:w-96 max-w-full h-auto drop-shadow-lg transition-transform duration-300 hover:scale-105" />
</header>

<main class="grid grid-cols-1 md:grid-cols-9 p-4 md:p-8 gap-4 bg-gray-50">

	<!-- 📚 Sidebar -->
	<aside class="md:col-span-1 flex bg-primary-100 p-4 rounded-2xl order-2 md:order-none">
		<div>
			<h2 class="font-bold mb-4 text-primary-500">Recent Posts</h2>
			<ul class="space-y-2">
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Post Title 1</a></li>
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Post Title 2</a></li>
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Post Title 3</a></li>
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Post Title 4</a></li>
			</ul>
		</div>
	</aside>

	<!-- Divider -->
	<div class="hidden md:block w-px bg-gray-900 ml-6"></div>

	<!-- ✍️ Main Blog Article -->
	<article class="md:col-span-6">
		<h1 class="text-3xl font-bold mb-4 text-secondary-900">Saludos cordiales</h1>
		<p class="text-gray-400 mb-4">By John Doe – May 2025</p>

		<div class="columns-1 md:columns-2 gap-6 text-justify break-words text-gray-500">
            <p>Lorem ipsum dolor sit amet...</p>
            <br>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe.</p>
			<p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe.</p>
			<p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe.</p>
			<p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe.</p>
			<p>Lorem ipsum dolor sit amet...</p>
			<p>Lorem ipsum dolor sit amet...</p>
			<p>Lorem ipsum dolor sit amet...</p>
			<p>Lorem ipsum dolor sit amet...</p>
		</div>
	</article>
</main>

<Newspaper  />