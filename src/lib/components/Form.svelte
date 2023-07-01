<script>
	// @ts-nocheck
	import MultiSelect from 'svelte-multiselect'
	import InputField from './InputField.svelte'
	export let active_step
	let formData = {
		name: '',
		surname: '',
		email: '',
		password: '',
		address: '',
		city: '',
		country: '',
		postcode: '',
		account_name: '',
		card_no: ''
	}

	let selected = []

	const iphoneOptions = [
		'iPhone 11',
		'iPhone 11 Pro',
		'iPhone 11 Pro Max',
		'iPhone 12 Mini',
		'iPhone 12',
		'iPhone 12 Pro',
		'iPhone 12 Pro Max',
		'iPhone 13 Mini',
		'iPhone 13',
		'iPhone 13 Pro',
		'iPhone 13 Pro Max',
		'iPhone 14',
		'iPhone 14 Plus',
		'iPhone 14 Pro',
		'iPhone 14 Pro Max',
		'Outro'
	]

	const gbOptions = ['64 GB', '128 GB', '256 GB', '512 GB', '1024 GB']

	const colorOptions = [
		'Preto',
		'Branco',
		'Verde',
		'Vermelho',
		'Lilas',
		'Amarelo',
		'Dourado',
		'Azul',
		'Roxo'
	]

	const batteryOptions = ['95% a 100%', '90% a 95%', '85% a 90%', '80% a 85%', 'Abaixo de 80%']

	let selectedIphone = []

	const handleSubmit = () => {
		console.log('Your form data => ', formData)
	}
</script>

<form class="form-container" on:submit={handleSubmit}>
	{#if active_step == 'Seu aparelho'}
		<p class="text-left">Qual modelo?</p>
		<MultiSelect bind:selectedIphone maxSelect={1} options={iphoneOptions} />
		<p class="text-left">Quantos GBs de armazenamento?</p>
		<MultiSelect maxSelect={1} options={gbOptions} />
		<p class="text-left">Qual a cor?</p>
		<MultiSelect maxSelect={1} options={colorOptions} />
	{:else if active_step == 'Address'}
		<p class="text-left">Qual a saúde da bateria?</p>
		<MultiSelect maxSelect={1} options={batteryOptions} />
	{:else if active_step == 'Payment'}
		<InputField label={'Account Name'} bind:value={formData.account_name} />
		<InputField label={'Card No'} bind:value={formData.card_no} />
	{:else if active_step == 'Confirmation'}
		<div class="message">
			<h2>Thank you for choosing us</h2>
			<button class="btn submit">Finish </button>
		</div>
	{/if}
</form>

<style>
	.form-container {
		background-color: #fff;
		border-radius: 10px;
		box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1), 0 6px 6px rgba(0, 0, 0, 0.1);
		padding: 50px 20px;
		text-align: center;
		max-width: 100%;
		width: 350px;
	}
	.btn {
		color: white;
		padding: 0.5rem 0;
		margin-top: 0.5rem;
		display: inline-block;
		width: 100%;
		border-radius: 0.25rem;
		cursor: pointer;
	}
	.submit {
		background: linear-gradient(to bottom, #44c767 5%, #50b01c 100%);
		background-color: #44c767;
	}
	.submit:hover {
		background: linear-gradient(to bottom, #50b01c 5%, #44c767 100%);
		background-color: #50b01c;
	}
	.message {
		text-align: center;
	}
</style>
