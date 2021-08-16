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