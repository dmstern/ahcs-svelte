<script>
	export let name;

	import { onMount }  from "svelte";

	let inputValue;

	onMount(() => {
		inputValue = "Test input";
	});

	const updateValue = event => {
		inputValue = event.target.value;
	}
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<fieldset>
		<input type="text" value={inputValue} on:input={updateValue} />
		<p>{inputValue}</p>
	</fieldset>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>