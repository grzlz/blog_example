<script>
    import Newspaper from "$lib/Newspaper.svelte";
</script>

<header class="text-center bg-secondary-900 p-6">
	<img src="/header.png" alt="Surcos Logo" class="mx-auto mb-12 w-72 md:w-96 max-w-full h-auto drop-shadow-lg transition-transform duration-300 hover:scale-105" />
</header>

<main class="grid grid-cols-1 md:grid-cols-9 p-4 md:p-8 gap-4 bg-gray-50">

	<!-- 📚 Sidebar -->
	<aside class="md:col-span-2 flex bg-secondary-100 md:bg-primary-100 p-4 rounded-2xl order-2 md:order-none h-auto self-start w-auto font-complementary">
		<div class="break-words">
			<h3 class="font-bold mb-4 text-primary-400">Artículos recientes</h3>
		<ul class="flex flex-wrap justify-start p-3 gap-6 mx-auto gap-y-2">
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Posta sdfas asdfsd</a></li>
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Post Title 2</a></li>
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Post Title 3</a></li>
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Post Title 4</a></li>
                				<li><a href="#" class="text-gray-500 hover:text-gray-900">Posta sdfas asdfsd</a></li>
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Post Title 2</a></li>
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Post Title 3</a></li>
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Post Title 4</a></li>
                				<li><a href="#" class="text-gray-500 hover:text-gray-900">Posta sdfas asdfsd</a></li>
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Post Title 2</a></li>
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Post Title 3</a></li>
				<li><a href="#" class="text-gray-500 hover:text-gray-900">Post Title 4</a></li>
			</ul>
		</div>
	</aside>

	<!-- Divider -->
	<div class="hidden md:block w-px bg-gray-900 ml-6"></div>

	<!-- ✍️ Main Blog Article -->
	<article class="md:col-span-6 prose">
		<h1 class="text-3xl font-bold mb-4 text-secondary-900 font-primary">Saludos cordiales</h1>
		<p class="text-gray-400 mb-4 font-secondary text-sm">By John Doe – May 2025</p>

		<div class="text-gray-500 prose font-secondary">
            <p>Lorem ipsum dolor sit amet...</p>
            <br>
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

<div class="bg-gray-50 py-24 sm:py-32">
  <div class="mx-auto max-w-7xl px-6 lg:px-8">
    <div class="mx-auto max-w-2xl lg:mx-0 prose">
      <h2 class="text-4xl font-semibold tracking-tight text-pretty text-gray-900 sm:text-5xl">From the blog</h2>
      <p class="mt-2 text-lg/8 text-gray-00">Learn how to grow your business with our expert advice.</p>
      <div class="text-gray-700">
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dicta facilis qui nisi, autem exercitationem asperiores labore totam recusandae consequatur fugit, minus corporis atque numquam omnis ad quidem quo, eius magni.</p>
    			<p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe.</p>
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe.</p>
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe.</p>
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe.</p>
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe.</p>
              
      </div>
    </div>
    <div class="mx-auto mt-10 grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 border-t border-gray-200 pt-10 sm:mt-16 sm:pt-16 lg:mx-0 lg:max-w-none lg:grid-cols-3">
      <article class="flex max-w-xl flex-col items-start justify-between">
        <div class="flex items-center gap-x-4 text-xs">
          <time datetime="2020-03-16" class="text-gray-500">Mar 16, 2020</time>
          <a href="#" class="relative z-10 rounded-full bg-gray-50 px-3 py-1.5 font-medium text-gray-600 hover:bg-gray-100">Marketing</a>
        </div>
        <div class="group relative">
          <h3 class="mt-3 text-lg/6 font-semibold text-gray-900 group-hover:text-gray-600">
            <a href="#">
              <span class="absolute inset-0"></span>
              Post relacionado 1
            </a>
          </h3>
          <p class="mt-5 line-clamp-3 text-sm/6 text-gray-600">Illo sint voluptas. Error voluptates culpa eligendi. Hic vel totam vitae illo. Non aliquid explicabo necessitatibus unde. Sed exercitationem placeat consectetur nulla deserunt vel. Iusto corrupti dicta.</p>
        </div>
        <div class="relative mt-8 flex items-center gap-x-4">
          <img src="https://images.unsplash.com/photo-1519244703995-f4e0f30006d5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="" class="size-10 rounded-full bg-gray-50">
          <div class="text-sm/6">
            <p class="font-semibold text-gray-900">
              <a href="#">
                <span class="absolute inset-0"></span>
                Michael Foster
              </a>
            </p>
            <p class="text-gray-600">Co-Founder / CTO</p>
          </div>
        </div>
      </article>
      <article class="flex max-w-xl flex-col items-start justify-between">
        <div class="flex items-center gap-x-4 text-xs">
          <time datetime="2020-03-16" class="text-gray-500">Mar 16, 2020</time>
          <a href="#" class="relative z-10 rounded-full bg-gray-50 px-3 py-1.5 font-medium text-gray-600 hover:bg-gray-100">Marketing</a>
        </div>
        <div class="group relative">
          <h3 class="mt-3 text-lg/6 font-semibold text-gray-900 group-hover:text-gray-600">
            <a href="#">
              <span class="absolute inset-0"></span>
              Post relacionado 2 o post siguiente
            </a>
          </h3>
          <p class="mt-5 line-clamp-3 text-sm/6 text-gray-600">Illo sint voluptas. Error voluptates culpa eligendi. Hic vel totam vitae illo. Non aliquid explicabo necessitatibus unde. Sed exercitationem placeat consectetur nulla deserunt vel. Iusto corrupti dicta.</p>
        </div>
        <div class="relative mt-8 flex items-center gap-x-4">
          <img src="https://images.unsplash.com/photo-1519244703995-f4e0f30006d5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="" class="size-10 rounded-full bg-gray-50">
          <div class="text-sm/6">
            <p class="font-semibold text-gray-900">
              <a href="#">
                <span class="absolute inset-0"></span>
                Michael Foster
              </a>
            </p>
            <p class="text-gray-600">Co-Founder / CTO</p>
          </div>
        </div>
      </article>


      <!-- More posts... -->
    </div>
  </div>
</div>