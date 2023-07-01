
<footer>
	<img src="/images/logo_trans.png" alt="Logo" width="128" height="128"/>
	<div class="navigation-footer">
		<h3>Sobre</h3>
		<div>
			<span>Texto</span>
		</div>
	</div>
	<div class="navigation-footer">
		<h3>Contatos</h3>
		<div>
			<span>Whatsapp</span>
			<span>Instagram</span>
			<span>Email</span>
		</div>
	</div>
	<div id="challenger">
		Feito por: fã do ret
	</div>
</footer>

<style scoped>
	footer {
		position: relative;
		display: grid;
		grid-template-columns: 25% 25% 25% 25%;
		padding: 2.5rem 5rem;
		background-color: #331444;
		border-radius: 0 10rem 0 0;
		color: #24ebeb;
	}
	.navigation-footer h3 {
		font-size: 1rem;
	}

	.navigation-footer div {
		margin-block-start: 2rem;
	}

	.navigation-footer div span {
		display: block;
		margin-block-end: 1rem;
		color: var(--grayish-blue);
	}
	.navigation-footer div span:hover {
		cursor: pointer;
		text-decoration: underline;
	}

	#challenger {
		position: absolute;
		left: 50%;
		bottom: 1vh;
		transform: translate(-50%);
	}

	@media screen and (max-aspect-ratio: 1) and (max-width: 767px) {
		footer {
			display: flex;
			flex-direction: column;
			padding: 4rem;
			text-align: center;
			align-items: center;
		}
		footer img {
			width: 40%;
			margin-bottom: 4rem;
		}

		#challenger {
			margin-block-start: 4rem;
			position: static;
			transform: none;
		}
	}
</style>
