<script></script>

<section class="relative h-screen py-40">
	<!-- <img
		src="/images/left_graphic.png"
		alt="Left Graphic"
		class="absolute bottom-0 left-0 w-full lg:w-fit lg:h-1/2"
	/> -->
	<img
		src="/images/apple.png"
		alt="Right Graphic"
		class="hidden lg:block absolute right-40 top-40 "
	/>
	<!-- <img src="/images/iphone_cable.png" alt="Right Graphic" class="lg:hidden absolute right-0 top-40 " /> -->
	<!-- <img src="/images/crab.png" alt="Crab" class="absolute left-0 hidden xl:block top-1/4" /> -->
	<div class="flex h-full px-8 mx-auto lg:max-w-6xl">
		<div class="z-10 flex flex-col justify-center h-full lg:w-1/2">
			<h1 class="headline">Lorem Ipsum</h1>

			<p class="font-medium text-lg sm:text-3xl md:text-[20px] leading-[171.5%] mt-6">
				Johnson's baby
			</p>
			<div class="flex space-x-[27px] mt-14">
				<a
					class="btn btn-gradient self-start"
					href="https://api.whatsapp.com/send?phone=5541992494753">Falar com um especialista</a
				>
				<!-- <button </button> -->
				<!-- <a class="flex items-center space-x-3 btn btn-outline" href="https://api.whatsapp.com/send?phone=5541992494753">
					<img src="/images/video_icon.svg" width={32} height={32} alt="Video Icon" />
					<span>Ver produtos</span>
				</a> -->
			</div>
		</div>
		<!-- <div class="relative w-1/2">
			<img src="/images/hero-image-desktop.png" class="w-full sm:hidden" alt="Hero" />
			<img src="/images/hero-image-mobile.png" class="absolute -bottom-4 -left-3" alt="Hero" />
		</div> -->
	</div>
	<div class="flex justify-evenly" >
		<img
			src="/images/apple-tv.svg"
			class="transform transition duration-300 hover:scale-110 cursor-pointer"
			alt="Apple TV"
		/>
		<img
			src="/images/apple-watch.svg"
			class="transform transition duration-300 hover:scale-110 cursor-pointer"
			alt="Apple Watch"
		/>
		<img
			src="/images/iphone.svg"
			class="transform transition duration-300 hover:scale-110 cursor-pointer"
			alt="iPhone"
		/>
	</div>
	<!-- </section>

<section> -->
</section>

<!-- <section class="py-20 text-black">
	<div class="max-w-screen-xl mx-auto">
		<div class="flex items-center space-x-24">
			<div class="flex flex-col w-1/2">
				<div class="flex flex-col space-y-4">
					<h1 class="text-5xl font-bold font-heading">Reach more people in real time</h1>
					<p>
						The Screeno ecosystem is designed to help you generate profit. Set up complete sales and
						marketing funnels with ease using the Screeno
					</p>
				</div>
				<div class="flex mt-12 space-x-3">
					<button class="w-1/3 primary">Start Free Trial</button>
					<button class="w-1/3 outline">Login</button>
				</div>
			</div>
			<div class="relative w-1/2">
				<img src="/images/hero-image-desktop.png" class="w-full h-full" alt="Hero" />
				<img src="/images/hero-image-mobile.png" class="absolute -bottom-4 -left-3" alt="Hero" />
			</div>
		</div>
		<div class="flex justify-between mt-32 space-x-24">
			
		</div>
	</div>
</section> -->
<style lang="postcss">
	.headline {
		@apply font-bold text-3xl sm:text-4xl md:text-5xl xl:text-[56px];
		line-height: 129%;
		background: linear-gradient(180deg, #1b18f9 0%, #1b18f9 46.35%, #e146ad 100%);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		background-clip: text;
		text-fill-color: transparent;
	}

	.btn {
		@apply px-9 py-4 font-semibold md:text-lg lg:text-2xl transition duration-300 hover:opacity-75;
		border-radius: 18px;
	}

	.btn-outline {
		background: linear-gradient(180deg, #1b18f9 0%, #1b18f9 46.35%, #e146ad 100%);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		background-clip: text;
		text-fill-color: transparent;
	}

	.btn-gradient {
		@apply text-white;
		background: radial-gradient(255.8% 457.4% at 88.45% 24.64%, #c27fcf 0%, #0368ff 100%)
			/* warning: gradient uses a rotation that is not supported by CSS and may not behave as expected */;
	}
</style>
