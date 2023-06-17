<script lang="ts">
	let name: any

	async function hmm() {
		const res = await fetch("https://jsonplaceholder.typicode.com/posts/1")
		name = await res.json()
	}
</script>

<button on:click={hmm}>???</button>

{#if name}
	<p>ID: {name.id}</p>
	<p>Title: {name.title}</p>
	<p>Body: {name.body}</p>
{/if}
