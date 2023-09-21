<script>
	import { Input, Label } from 'flowbite-svelte';
	import { onMount } from 'svelte';
	import Card from './Card.svelte';

	$: dollarValue = 0;
	let userInput = 0;

	onMount(async () => {
		const response = await fetch('https://dolar-api.up.railway.app/');
		const data = await response.json();
		dollarValue = parseFloat(data[0].venta);
		console.log(dollarValue);
	});

	$: impuestoPais = Number(userInput * dollarValue * 0.3);
	$: impuestoGanancias = Number(userInput * dollarValue * 0.45);
	$: total = Number(userInput * dollarValue + impuestoPais + impuestoGanancias);
</script>

<div class="my-6 mt-12">
	<Label for="default-input" class="text-left block mb-2"
		>Cantidad de dólares(USD)</Label
	>
	<Input
		id="default-input"
		placeholder="Ingrese cantidad de USD"
		type="number"
		min="0"
		bind:value={userInput}
	/>
	<Card {impuestoPais} {impuestoGanancias} {total} {dollarValue} />
</div>
