<script>
	import ChildComponent from '../components/ChildComponent.svelte';
	import Card from '../components/Card.svelte';

	let name = "";

	let checked = false;

	const persons = [
    { name: 'Alice' },
    { name: 'Bob'},
    { name: 'Carol' }
  ];
  </script>
  
  <main>
	  <Card>
			<ChildComponent username="Watataku" />
		</Card>
		
		<hr>

		<!-- バインディング -->
		<input placeholder="Enter your name" bind:value={name}>
		<div>Hello, {name}</div>

		<hr>

		<!-- 条件分岐 -->
		<label>
			<input type="checkbox" bind:checked={checked}>
			Check Me!
		</label>
		{#if checked}
			<div>Checked!</div>
		{:else}
			<div>Hurry!</div>
		{/if}
		
		<hr>

		<!-- ループ処理 -->
		{#each persons as p}
			<div>{p.name}</div>
		{/each}
	</main>
	
  <style>
  </style>