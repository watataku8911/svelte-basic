<<<<<<< HEAD
=======

>>>>>>> 4058d597d73754e2efc4beb35c0a448613ac118d
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
<<<<<<< HEAD

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

### Component & props

Create a new file `Greeting.svelte` under the `src` folder. Then write the following:

```
<script>
  export let username;
</script>

<div>
  Hello, {username}!
</div>
```

On the other hand, in the parent component, please rewrite as follows

```
<script>
  import Greeting from './Greeting.svelte';
</script>

<main>
  <Greeting username="Watataku"/>
</main>

<style>
</style>
```

### Binding

```
<script>
  let name = '';
</script>

<main>
  <input placeholder="Enter your name" bind:value={name}>
  <div>Hello, {name}</div>
</main>

<style>
</style>
```

The name variable is associated with the input element using bind: value. Now, if the input value of the input element changes, the name variable will also change.

### if & for

- if

The start is {#if condition} and the end is {/ if}. else puts {: else} in between, and else-if puts {: else if condition} in between.

```
<script>
  let checked = false;
</script>

<main>
  <label>
    <input type="checkbox" bind:checked={checked}>
    Check Me!
  </label>
  {#if checked}
    <div>Checked!</div>
  {:else}
    <div>Hurry!</div>
  {/if}
</main>

<style>
</style>
```

- for

The iterative process is sandwiched between {#each array as item} and {/ each}.

```
<script>
  const persons = [
    { name: 'Alice' },
    { name: 'Bob'},
    { name: 'Carol' }
  ];
</script>

<main>
  {#each persons as p}
    <div>{p.name}</div>
  {/each}
</main>

<style>
</style>
```

### Routing

```
$ npm install svelte-spa-router
```

#### Creating a routing definition

Create a correspondence of which component is tied to which routing.
Create `router / index.js` under the `src` folder.

```
import Basic from "../pages/Basic.svelte";
import SecoundBasic from "../pages/SecoundBasic.svelte";

export const routes = {
  "/": Basic,
  "/secound": SecoundBasic,
};
```

#### Creating a Router View

After defining the route, let's draw the defined route.
Modify `App.svelte`.

```
<script>
  import Router, {push} from 'svelte-spa-router'
	import { routes } from './router'

	const onClickBasic = () => {
		push("/");
	}

	const onClickSecoundPage = () => {
		push("/secound");
	}


</script>

<main>
	<button on:click={onClickBasic}>Basic</button>
	<button on:click={onClickSecoundPage}>Secound page</button>
  <Router routes={routes} />
</main>
=======
>>>>>>> 4058d597d73754e2efc4beb35c0a448613ac118d
```
