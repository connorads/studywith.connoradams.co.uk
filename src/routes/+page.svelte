<script lang="ts">
	import study1 from '$lib/assets/study1.jpeg';
	import study2 from '$lib/assets/study2.jpeg';

	let alt1 = 'Study Gang #1';
	let alt2 = 'Study Gang #2';

	let showModal = false;
	let selectedImage: null | string = null;
	let selectedAlt: null | string = null;

	function openModal(imageSrc: string, imageAlt: string) {
		selectedImage = imageSrc;
		selectedAlt = imageAlt;
		showModal = true;
		window.addEventListener('keydown', handleKeyDown);
	}

	function closeModal() {
		showModal = false;
		window.removeEventListener('keydown', handleKeyDown);
	}

	function handleKeyDown(event: KeyboardEvent) {
		if (event.key === 'Escape') {
			closeModal();
		}
	}
</script>

<svg
	xmlns="http://www.w3.org/2000/svg"
	version="1.1"
	xmlns:xlink="http://www.w3.org/1999/xlink"
	viewBox="0 0 40 40"
	display="none"
	width="0"
	height="0"
	><symbol id="map" viewBox="0 0 40 40"
		><path
			d="M25.5,14.7c0-1.5-0.5-2.7-1.6-3.8c-1-1-2.3-1.6-3.8-1.6c-1.5,0-2.7,0.5-3.8,1.6c-1,1-1.6,2.3-1.6,3.8s0.5,2.7,1.6,3.8 c1,1,2.3,1.6,3.8,1.6c1.5,0,2.7-0.5,3.8-1.6C25,17.4,25.5,16.1,25.5,14.7z M30.9,14.7c0,1.5-0.2,2.8-0.7,3.7l-7.6,16.2 c-0.2,0.5-0.6,0.8-1,1.1c-0.4,0.3-0.9,0.4-1.4,0.4c-0.5,0-1-0.1-1.4-0.4c-0.4-0.3-0.8-0.6-1-1.1l-7.6-16.2c-0.5-1-0.7-2.2-0.7-3.7 c0-3,1-5.5,3.1-7.6S17.2,4,20.2,4c3,0,5.5,1,7.6,3.1S30.9,11.7,30.9,14.7L30.9,14.7z"
		></path></symbol
	><symbol id="github" viewBox="0 0 40 40"
		><path
			d="M36,20.3c0,3.5-1,6.6-3.1,9.4c-2,2.8-4.7,4.7-7.9,5.8c-0.4,0.1-0.6,0-0.8-0.1c-0.2-0.2-0.3-0.4-0.3-0.6v-4.4 c0-1.3-0.4-2.3-1.1-3c0.8-0.1,1.5-0.2,2.1-0.4c0.6-0.2,1.3-0.4,2-0.8c0.7-0.4,1.2-0.8,1.7-1.4c0.5-0.5,0.8-1.3,1.1-2.2 s0.4-2,0.4-3.1c0-1.7-0.5-3.1-1.6-4.3c0.5-1.3,0.5-2.7-0.2-4.2c-0.4-0.1-1,0-1.7,0.2c-0.7,0.3-1.4,0.6-1.9,0.9L24,12.5 c-1.3-0.4-2.6-0.5-4-0.5s-2.7,0.2-4,0.5c-0.2-0.2-0.5-0.3-0.9-0.6c-0.4-0.2-0.9-0.5-1.7-0.8c-0.8-0.3-1.4-0.4-1.8-0.3 c-0.6,1.6-0.7,3-0.1,4.2c-1.1,1.2-1.6,2.6-1.6,4.3c0,1.2,0.1,2.2,0.4,3.1s0.6,1.6,1.1,2.2s1,1,1.7,1.4c0.7,0.4,1.3,0.6,2,0.8 c0.6,0.2,1.3,0.3,2.1,0.4c-0.6,0.5-0.9,1.2-1,2.1c-0.3,0.1-0.6,0.2-0.9,0.3c-0.3,0.1-0.7,0.1-1.2,0.1c-0.5,0-0.9-0.1-1.4-0.4 c-0.5-0.3-0.8-0.7-1.2-1.3c-0.3-0.4-0.6-0.8-1-1.1c-0.4-0.3-0.8-0.4-1-0.5L9,26.5c-0.3,0-0.5,0-0.6,0.1c-0.1,0.1-0.1,0.1-0.1,0.2 c0,0.1,0.1,0.2,0.2,0.3c0.1,0.1,0.2,0.2,0.3,0.2l0.1,0.1c0.3,0.1,0.6,0.4,0.9,0.8s0.5,0.7,0.7,1.1l0.2,0.5c0.2,0.5,0.5,1,0.9,1.3 c0.4,0.3,0.9,0.5,1.4,0.6c0.5,0.1,1,0.1,1.4,0.1c0.5,0,0.9,0,1.2-0.1l0.5-0.1c0,0.5,0,1.1,0,1.9c0,0.7,0,1.1,0,1.1 c0,0.2-0.1,0.5-0.3,0.6c-0.2,0.2-0.5,0.2-0.8,0.1c-3.2-1.1-5.8-3-7.9-5.8S4,23.8,4,20.3c0-2.9,0.7-5.6,2.1-8S9.5,7.8,12,6.4 s5.1-2.1,8-2.1s5.6,0.7,8,2.1s4.4,3.4,5.8,5.8S36,17.4,36,20.3L36,20.3z"
		></path></symbol
	><symbol id="linkedin" viewBox="0 0 40 40"
		><path
			d="M12.1,13.8v19.1H5.7V13.8C5.7,13.8,12.1,13.8,12.1,13.8z M12.5,7.9c0,0.9-0.3,1.7-1,2.4c-0.7,0.6-1.5,0.9-2.6,0.9h0 c-1.1,0-1.9-0.3-2.5-0.9c-0.6-0.6-1-1.4-1-2.4c0-1,0.3-1.7,1-2.4S7.9,4.6,9,4.6s1.9,0.3,2.6,0.9S12.5,6.9,12.5,7.9z M35,22v11h-6.4 V22.7c0-1.4-0.3-2.4-0.8-3.2c-0.5-0.8-1.3-1.1-2.4-1.1c-0.8,0-1.5,0.2-2,0.7c-0.5,0.4-1,1-1.2,1.7c-0.1,0.4-0.2,0.9-0.2,1.6v10.7 h-6.4c0-5.1,0-9.3,0-12.5s0-5.1,0-5.7l0-0.9H22v2.8h0c0.3-0.4,0.5-0.8,0.8-1.1c0.3-0.3,0.6-0.6,1.1-1c0.5-0.4,1-0.6,1.7-0.8 c0.7-0.2,1.4-0.3,2.2-0.3c2.2,0,4,0.7,5.3,2.2C34.4,17,35,19.1,35,22L35,22z"
		></path></symbol
	><symbol id="home" viewBox="0 0 40 40"
		><path
			d="M33.3,22.3v11.2c0,0.4-0.1,0.8-0.4,1.1c-0.3,0.3-0.6,0.4-1.1,0.4h-9v-9h-6v9h-9c-0.4,0-0.8-0.1-1.1-0.4 c-0.3-0.3-0.4-0.6-0.4-1.1V22.3c0,0,0,0,0-0.1s0-0.1,0-0.1L19.9,11l13.5,11.1C33.3,22.1,33.3,22.2,33.3,22.3L33.3,22.3z M38.5,20.6 l-1.5,1.7c-0.1,0.1-0.3,0.2-0.5,0.3h-0.1c-0.2,0-0.4-0.1-0.5-0.2L19.9,9L3.7,22.5c-0.2,0.1-0.4,0.2-0.6,0.2c-0.2,0-0.4-0.1-0.5-0.3 l-1.5-1.7C1,20.5,1,20.3,1,20.1s0.1-0.4,0.3-0.5l16.8-14C18.6,5.2,19.2,5,19.9,5s1.3,0.2,1.8,0.6l5.7,4.8V5.8c0-0.2,0.1-0.4,0.2-0.5 S27.9,5,28.1,5h4.5c0.2,0,0.4,0.1,0.5,0.2c0.1,0.1,0.2,0.3,0.2,0.5v9.5l5.1,4.3c0.2,0.1,0.2,0.3,0.3,0.5 C38.7,20.3,38.7,20.5,38.5,20.6L38.5,20.6z"
		></path></symbol
	><symbol id="medium" viewBox="0 0 40 40"
		><path
			d="M22.6,20c0,6.3-5.1,11.4-11.3,11.4S0,26.3,0,20S5.1,8.6,11.3,8.6S22.6,13.7,22.6,20 M34.9,20c0,5.9-2.5,10.7-5.6,10.7 c-3.1,0-5.6-4.8-5.6-10.7s2.5-10.7,5.6-10.7C32.4,9.3,34.9,14.1,34.9,20 M40,20c0,5.3-0.9,9.6-2,9.6s-2-4.3-2-9.6s0.9-9.6,2-9.6 S40,14.7,40,20"
		></path></symbol
	><symbol id="twitter" viewBox="0 0 40 40"
		><path
			d="M36.3,10.2c-1,1.3-2.1,2.5-3.4,3.5c0,0.2,0,0.4,0,1c0,1.7-0.2,3.6-0.9,5.3c-0.6,1.7-1.2,3.5-2.4,5.1 c-1.1,1.5-2.3,3.1-3.7,4.3c-1.4,1.2-3.3,2.3-5.3,3c-2.1,0.8-4.2,1.2-6.6,1.2c-3.6,0-7-1-10.2-3c0.4,0,1.1,0.1,1.5,0.1 c3.1,0,5.9-1,8.2-2.9c-1.4,0-2.7-0.4-3.8-1.3c-1.2-1-1.9-2-2.2-3.3c0.4,0.1,1,0.1,1.2,0.1c0.6,0,1.2-0.1,1.7-0.2 c-1.4-0.3-2.7-1.1-3.7-2.3s-1.4-2.6-1.4-4.2v-0.1c1,0.6,2,0.9,3,0.9c-1-0.6-1.5-1.3-2.2-2.4c-0.6-1-0.9-2.1-0.9-3.3s0.3-2.3,1-3.4 c1.5,2.1,3.6,3.6,6,4.9s4.9,2,7.6,2.1c-0.1-0.6-0.1-1.1-0.1-1.4c0-1.8,0.8-3.5,2-4.7c1.2-1.2,2.9-2,4.7-2c2,0,3.6,0.8,4.8,2.1 c1.4-0.3,2.9-0.9,4.2-1.5c-0.4,1.5-1.4,2.7-2.9,3.6C33.8,11.2,35.1,10.9,36.3,10.2L36.3,10.2z"
		></path></symbol
	></svg
>

<main class="flex flex-col items-center justify-center min-h-screen p-4 bg-gray-100 text-gray-800">
	<div class="container max-w-sm md:max-w-2xl lg:max-w-4xl bg-white p-8 shadow rounded">
		<h1 class="text-2xl md:text-3xl lg:text-4xl font-bold text-center mb-4">
			Study with Connor 🎓
		</h1>

		<p class="text-lg md:text-xl text-center">
			We've all got projects and things we'd like to get on with. <br /> But sometimes it's hard to
			find the motivation. <br /> Solution? Let's hangout and work together 💻☕📚😎
		</p>

		<div class="flex flex-col md:flex-row justify-center gap-4 py-4 px-4 md:px-20">
			<button
				on:click={() => openModal(study1, alt1)}
				on:keydown={(event) => event.key === 'Enter' && openModal(study1, alt1)}
			>
				<img src={study1} alt={alt1} class="w-full h-64 object-cover cursor-pointer" />
			</button>
			<button
				on:click={() => openModal(study2, alt2)}
				on:keydown={(event) => event.key === 'Enter' && openModal(study2, alt2)}
			>
				<img src={study2} alt={alt2} class="w-full h-64 object-cover cursor-pointer" />
			</button>
		</div>

		{#if showModal}
			<button on:click={() => closeModal()}>
				<div class="fixed inset-0 bg-black bg-opacity-50 overflow-y-auto h-full w-full">
					<div
						class="relative top-20 mx-auto p-5 border w-3/4 md:w-1/2 lg:w-2/3 xl:w-1/2 2xl:w-1/3 shadow-lg rounded-md bg-white"
					>
						<img src={selectedImage} alt={selectedAlt} class="w-full h-auto" />
					</div>
				</div>
			</button>
		{/if}

		<p class="text-lg md:text-xl text-center mb-8">
			Probably in some cafe in London 💂 <br /> Or on Google Meet or Zoom 💻 <br /> Usually evenings
			and weekends ⏳
		</p>

		<p class="text-lg md:text-xl text-center mb-8">
			Fancy joining for a session or two? 👋 <br /> Contact me and we can organise something 📆
		</p>

		<a href="https://connoradams.co.uk"
			><h2
				class="text-xl md:text-2xl lg:text-3xl text-center font-semibold mb-4 text-blue-500 hover:text-blue-600"
			>
				Contact me 📩
			</h2></a
		>

		<div class="my-8">
			<h2 class="text-xl md:text-2xl lg:text-3xl text-center font-semibold mb-4">
				Things I sometimes work on 💡
			</h2>
			<ul class="list-disc list-inside text-center mb-8">
				<li class="text-base md:text-lg">
					My Slack bot called <a
						href="https://lockbot.app"
						class="text-blue-500 hover:text-blue-600">Lockbot</a
					>
				</li>
				<li class="text-base md:text-lg">
					Coding practice with <a
						href="https://exercism.io"
						class="text-blue-500 hover:text-blue-600">Exercism.io</a
					>
				</li>
				<li class="text-base md:text-lg">
					Doing an <a
						href="https://www.coursera.org/account/accomplishments/specialization/6EFN3JCVPVQN"
						class="text-blue-500 hover:text-blue-600"
					>
						online course
					</a>
				</li>
				<li class="text-base md:text-lg">
					Other <a href="https://github.com/connorads" class="text-blue-500 hover:text-blue-600">
						random stuff
					</a>
				</li>
			</ul>

			<h2 class="text-xl md:text-2xl lg:text-3xl text-center font-semibold mb-4">
				Things other people work on
			</h2>
			<ul class="list-disc list-inside text-center">
				<li class="text-base md:text-lg">Studying for Masters</li>
				<li class="text-base md:text-lg">Learning to code</li>
				<li class="text-base md:text-lg">Freelancing work</li>
				<li class="text-base md:text-lg">Insert your project/goal here 😉</li>
			</ul>
		</div>

		<footer class="flex justify-center space-x-4 mt-8">
			<a href="https://connoradams.co.uk" class="hover:text-blue-600">
				<svg class="w-6 h-6 md:w-8 md:h-8 lg:w-10 lg:h-10 fill-current"
					><use xlink:href="#home"></use></svg
				>
			</a>
			<a href="https://www.linkedin.com/in/connoradams" class="hover:text-blue-600">
				<svg class="w-6 h-6 md:w-8 md:h-8 lg:w-10 lg:h-10 fill-current"
					><use xlink:href="#linkedin"></use></svg
				>
			</a>
			<a href="https://github.com/connorads" class="hover:text-blue-600">
				<svg class="w-6 h-6 md:w-8 md:h-8 lg:w-10 lg:h-10 fill-current"
					><use xlink:href="#github"></use></svg
				>
			</a>
			<a href="https://twitter.com/connorads" class="hover:text-blue-600">
				<svg class="w-6 h-6 md:w-8 md:h-8 lg:w-10 lg:h-10 fill-current"
					><use xlink:href="#twitter"></use></svg
				>
			</a>
			<a href="https://medium.com/@connorads" class="hover:text-blue-600">
				<svg class="w-6 h-6 md:w-8 md:h-8 lg:w-10 lg:h-10 fill-current"
					><use xlink:href="#medium"></use></svg
				>
			</a>
			<a href="https://thepengestkhans.co.uk" class="hover:text-blue-600">
				<svg class="w-6 h-6 md:w-8 md:h-8 lg:w-10 lg:h-10 fill-current"
					><use xlink:href="#map"></use></svg
				>
			</a>
		</footer>
	</div>
</main>
