<script>
	import About from "./components/About.svelte";
	import Text from "./components/Text.svelte";
	import Person from "./components/Person.svelte";
	import Skills from "./components/Skills.svelte";
	import Input from "./components/Input.svelte";

	export let name;
	export let lastName;
	let svelteLogo = "https://arepa.s3.amazonaws.com/svelte-logo.png";

	const personData = {
		firstName: 'Paul',
		lastName: 'Realpe',
		age: 26,
	};
</script>

<main>
	<h1>Hello {name} {lastName}!</h1>
	<img src={ svelteLogo } alt="Svelte logo">
	<Input name="name" />
	<Person personData={ personData } />
	<Text anotherText="Initial date: 04/29/2023" />
	<Skills />
	<About />
</main>

<style>
	:global(body) {
		background-color: azure;
		color: darkslateblue;
	}

	/* definir estilos globales con variables */
	:global(:root) {
		--theme-color: purple;
	}

	:global(body.dark-theme) {
		background-color: #1d3040;
		color: #bfc2c7;
	}

	p {
		color: var(--theme-color);
	}

	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	main img {
		width: 30%;
	}

	h1 {
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