## svelte app

This is a project template for [Svelte](https://svelte.dev) apps. It lives at https://github.com/sveltejs/template.

To create a new project based on this template using [degit](https://github.com/Rich-Harris/degit):

```bash
npx degit sveltejs/template svelte-app
cd svelte-app
```

_Note that you will need to have [Node.js](https://nodejs.org) installed._

### Get started

Install the dependencies...

```bash
cd svelte-app
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

### Building and running in production mode

To create an optimised version of the app:

```bash
npm run build
```

### clickEvent

```
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
```
