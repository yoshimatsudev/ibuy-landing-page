<script>
// @ts-nocheck

	import Form from '$lib/components/Form.svelte';
	import ProgressBar from '$lib/components/ProgressBar.svelte';
	let steps = ['Seu aparelho', 'Address', 'Payment', 'Confirmation'], currentActive = 1, progressBar;
	
	const handleProgress = (stepIncrement) => {
		progressBar.handleProgress(stepIncrement)
	}
	
</script>

<section class="">
<main>
	<div class="container">
		<ProgressBar {steps} bind:currentActive bind:this={progressBar}/>
		
		<Form active_step={steps[currentActive-1]}/>

		<div class="step-button">
			<button class="btn" on:click={() => handleProgress(-1)} disabled={currentActive == 1}>Voltar</button>
			<button class="btn" on:click={() => handleProgress(+1)} disabled={currentActive == steps.length}>Continuar</button>
		</div>		
	</div>	  
</main>
</section>
<style>

	@import url('https://fonts.googleapis.com/css?family=Muli&display=swap');
	
	* {
		box-sizing: border-box;
	}

	main {
		font-family: 'Muli', sans-serif;
		display: flex;
		align-items: center;
		justify-content: center;
		height: 100vh;
        text-align: -webkit-center;
		overflow: hidden;
		margin: 0;
	}

	.btn {
		background-color: #3498db;
		color: #fff;
		border: 0;
		border-radius: 6px;
		cursor: pointer;
		font-family: inherit;
		padding: 8px 30px;
		margin: 5px;
		font-size: 14px;
	}

	.btn:active {
		transform: scale(0.98);
	}

	.btn:focus {
		outline: 0;
	}

	.btn:disabled {
		background-color: #e0e0e0;
		cursor: not-allowed;
	}
	
	.step-button{
		margin-top: 1rem;
		text-align: center;
	}
</style>