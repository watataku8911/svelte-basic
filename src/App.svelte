<script>
	import ChildComponent from './components/ChildComponent.svelte';
	import Card from './components/Card.svelte';

	let name = "";
  </script>
  
  <main>
	  <Card>
			<ChildComponent username="Watataku" />
	  </Card>

		<input placeholder="Enter your name" bind:value={name}>
		<div>Hello, {name}</div>
	</main>
  <style>
  </style>