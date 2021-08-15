<script>
	const messages = ['Hello!', 'Svelte!'];
	let current = 0;

	const toggle = () => current = (current+1) % 2;
</script>

<main>
	{messages[current]}
	<button on:click={toggle}>Toggle Message</button>
</main>

<style>
</style>
