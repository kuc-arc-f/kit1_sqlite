<svelte:head>
	<title>Posts</title>
	<meta name="description" content="About this app" />
</svelte:head>

<script>
/** @type {import('./$types').PageData} */
export let data;
console.log(data);
//console.log(data.items);
  </script>

<div>
	<h1>posts</h1>
	<hr />
	{#each data.items as item}
	<div>
		<h3>{item.title}</h3>
		<p>ID : {item.id}</p>
		<a href={`/posts/${item.id}`} class="btn">[ show ]
		</a>		
		<hr />
	</div>
	{/each}	
</div>
