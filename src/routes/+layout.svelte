<script>
	import { slide } from 'svelte/transition';
	import '../app.css';
	let { children } = $props();
	let mobileMenuOpen = $state(false);

	let links = [
		{ text: 'Justicia', href: '#', logo: "/logo_justicia.png"  },
		{ text: 'Desarrollo', href: '#', logo: "/logo_desarrollo.png" },
		{ text: 'Cultura', href: '#', logo: "/logo_cultura.png" },
		{ text: 'Economía', href: '#', logo: "/logo_economia.png" },
		{ text: 'Política', href: '#', logo: "/logo_politica.png" },
		{ text: 'Medio ambiente', href: '#', logo: "/logo_medio_ambiente.png" },
	] 

	    const year = new Date().getFullYear();
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
			<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" class="h-6 w-6" >
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
						<img src={link.logo} alt={link.text} class="h-5 w-5" />
					</a>
				</li>
			{/each}
		</ul>
		{/if}

	<!-- Mobile dropdown menu -->

	{@render children()}


<footer class="bg-primary-50 text-gray-300 font-primary">
  <div class="max-w-6xl mx-auto px-6 py-12 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8">
    
    <!-- About Us -->
    <div>
      <h2 class="text-xl font-bold mb-4 text-primary-500">¿Quién chota sos?</h2>
      <p class="text-sm leading-relaxed text-gray-900 font-secondary">
		Somos un grupo de jóvenes profesionistas y académicos que creen que las cosas pueden ser distintas.
      </p>
    </div>


	
    <!-- Newsletter -->
<div>
  <h2 class="text-lg sm:text-xl font-bold text-primary-500 font-primary mb-2">Trade offer:</h2>
  <p class="text-sm sm:text-base text-gray-900 font-secondary mb-3">
    Si nos das tu correo, te damos acceso a nuestro resumen semanal de noticias.
  </p>
  <form class="flex flex-col sm:flex-row sm:items-center gap-2">
    <input
      type="email"
      placeholder="Tu correo electrónico"
      class="flex-1 px-4 py-2 rounded-md bg-gray-800 text-white placeholder-gray-400 text-sm focus:outline-none focus:ring-2 focus:ring-primary-500"
    />
    <button
      type="submit"
      class="bg-primary-400 hover:bg-primary-600 text-white px-4 py-2 rounded-md text-sm whitespace-nowrap transition">
      Suscribirme al newsletter
    </button>
  </form>
</div>

	<!-- Social Media -->
    <div>
      <h2 class="text-xl font-bold mb-4 text-primary-400">Nuestras redes sociales</h2>
      <div class="flex gap-4">
        <a href="#" aria-label="Twitter" class="hover:text-white">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M8 19c11 0 14-9 14-14v-.5A10 10 0 0122 4a9.86 9.86 0 01-2.828.775A4.94 4.94 0 0021.5 2a9.77 9.77 0 01-3.127 1.195A4.92 4.92 0 0016.5 2a4.92 4.92 0 00-4.92 4.92c0 .386.043.762.127 1.122A13.978 13.978 0 013 3.6a4.92 4.92 0 001.523 6.574A4.9 4.9 0 012 9.4v.062a4.92 4.92 0 003.946 4.827 4.93 4.93 0 01-2.213.084 4.93 4.93 0 004.6 3.417A9.867 9.867 0 012 18.543 13.949 13.949 0 008 19z" />
          </svg>
        </a>
        <a href="#" aria-label="GitHub" class="hover:text-white">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
            <path fill-rule="evenodd"
              d="M12 0C5.373 0 0 5.373 0 12c0 5.302 3.438 9.8 8.207 11.385.6.11.793-.26.793-.577v-2.01c-3.338.725-4.033-1.608-4.033-1.608-.547-1.388-1.333-1.758-1.333-1.758-1.09-.745.083-.729.083-.729 1.205.085 1.84 1.237 1.84 1.237 1.07 1.835 2.809 1.305 3.495.997.108-.775.42-1.305.763-1.604-2.665-.3-5.467-1.332-5.467-5.93 0-1.31.469-2.381 1.236-3.221-.124-.303-.536-1.52.117-3.168 0 0 1.008-.322 3.3 1.23a11.52 11.52 0 013.003-.404c1.02.005 2.047.138 3.003.404 2.29-1.552 3.296-1.23 3.296-1.23.655 1.648.243 2.865.12 3.168.77.84 1.233 1.911 1.233 3.22 0 4.61-2.807 5.625-5.48 5.92.43.372.823 1.103.823 2.222v3.293c0 .32.192.694.8.576C20.565 21.796 24 17.298 24 12c0-6.627-5.373-12-12-12z"
              clip-rule="evenodd" />
          </svg>
        </a>
        <a href="#" aria-label="LinkedIn" class="hover:text-white">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
            <path
              d="M4.98 3.5C4.98 4.88 3.87 6 2.49 6 1.11 6 0 4.88 0 3.5S1.11 1 2.49 1C3.87 1 4.98 2.12 4.98 3.5zM.17 8h4.64v13.99H.17V8zm7.93 0h4.45v1.91h.06c.62-1.18 2.13-2.43 4.4-2.43 4.7 0 5.57 3.09 5.57 7.1V22H18V15.3c0-1.59-.03-3.63-2.21-3.63-2.21 0-2.55 1.73-2.55 3.52V22H8.1V8z" />
          </svg>
        </a>
      </div>
    </div>
  
</div>

  
<div class="border-t border-primary-300 text-sm text-gray-300 px-4 py-6">
  <div class="max-w-6xl mx-auto flex flex-col sm:flex-row justify-between items-center gap-2">
    
    <!-- Left section: © + logo + year -->
    <div class="flex items-center">
      <span class="text-sm -mr-1">©</span>
      <img src="/header.png" alt="Surcos logo" class="w-[90px] h-auto -ml-1" />
      <span class="-ml-1 mt-0.5">{year}</span>
    </div>
    
    <!-- Right section: Attribution -->
    <p class="text-center sm:text-right">
      Desarrollado por <a href="http://www.icarus.mx" class="hover:text-white ">icarus.mx</a>
    </p>

  </div>
</div>


</div>
