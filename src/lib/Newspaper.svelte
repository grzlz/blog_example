<!-- src/lib/Newspaper.svelte -->
<script>
  // Mock article data (array of objects)
  let articles = [
    { id: 1, title: "First Post", content: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe.Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe." },
    { id: 2, title: "Second Post", content: "This is a bit longer summary of the second post, which has more content to show how the card height can vary with more text." },
    { id: 3, title: "Third Post", content: "Another article excerpt goes here. It could be a few lines long." },
    { id: 4, title: "Fourth Post", content: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe." },
    { id: 5, title: "Fifth Post", content: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe. Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit debitis praesentium ullam sunt omnis saepe atque corporis exercitationem, aliquid dolorum eum provident minus sit. Dolor esse placeat laudantium at saepe." },
    { id: 6, title: "Sixth Post", content: "Summary of the sixth post. Vivamus blandit aliquet ipsum, at sodales sapien luctus non." }
  ];
</script>

<!-- Masonry container: 1 column on mobile, 2 on sm, 3 on lg, with gap between columns -->
<div class="bg-primary-300 p-8">
	<div class="columns-2 gap-6 [column-fill:_balance]">
		{#each articles as article}
			<div class="mb-6 break-inside-avoid rounded-lg bg-secondary-900 shadow p-4 inline-block w-full">
				<h3 class="text-xl font-bold mb-2">{article.title}</h3>
				<p class="text-gray-300 text-sm">{article.content}</p>
			</div>
		{/each}
	</div>
</div>