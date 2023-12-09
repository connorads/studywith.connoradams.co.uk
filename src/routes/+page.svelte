<script lang="ts">
	import study1 from '$lib/assets/study1.jpeg';
	import study3 from '$lib/assets/study3.jpeg';

	let alt1 = 'Study Gang #1';
	let alt3 = 'Study Gang #2';

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

<main class="flex flex-col items-center justify-center min-h-screen p-4 bg-gray-100 text-gray-800">
	<div class="container max-w-4xl bg-white p-8 shadow rounded">
		<h1 class="text-4xl font-bold text-center mb-4">Study with Connor 🎓</h1>
		<p class="text-xl text-center">
			We've all got projects and things we'd like to get on with. <br /> But sometimes it's hard to
			find the motivation. <br /> Solution? Let's hangout and work together 💻☕📚😎
		</p>

		<div class="flex justify-center gap-4 py-4 px-20">
			<button
				on:click={() => openModal(study1, alt1)}
				on:keydown={(event) => event.key === 'Enter' && openModal(study1, alt1)}
			>
				<img src={study1} alt={alt1} class="w-full h-64 cursor-pointer" />
			</button>
			<button
				on:click={() => openModal(study3, alt3)}
				on:keydown={(event) => event.key === 'Enter' && openModal(study3, alt3)}
			>
				<img src={study3} alt={alt3} class="w-full h-64 cursor-pointer" />
			</button>
		</div>

		{#if showModal}
			<button on:click={() => closeModal()}>
				<div class="fixed inset-0 bg-black bg-opacity-50 overflow-y-auto h-full w-full">
					<div
						class="relative top-20 mx-auto p-5 border w-11/12 md:w-1/2 shadow-lg rounded-md bg-white"
					>
						<img src={selectedImage} alt={selectedAlt} class="w-full h-auto" />
					</div>
				</div>
			</button>
		{/if}

		<p class="text-xl text-center mb-8">
			I've blocked out some weekends in my calendar to do some work (10am-5pm) 💪
		</p>

		<p class="text-xl text-center mb-8">
			Probably in some cafe in London 💂 <br /> Or on Google Meet or Zoom 💻
		</p>

		<p class="text-xl text-center mb-8">
			Fancy joining for a session or two? 👋 <br /> Contact me and I'll send you a calendar invite 📆
		</p>

		<div class="my-8">
			<h2 class="text-3xl text-center font-semibold mb-4">Things I somtimes work on 💡</h2>
			<ul class="list-disc list-inside text-center mb-8">
				<li>
					My Slack bot called <a
						href="https://lockbot.app"
						class="text-blue-500 hover:text-blue-600">Lockbot</a
					>
				</li>
				<li>
					Coding practice with <a
						href="https://exercism.io"
						class="text-blue-500 hover:text-blue-600">Exercism.io</a
					>
				</li>
				<li>Doing an online course</li>
				<li>Other random stuff</li>
			</ul>

			<h2 class="text-3xl text-center font-semibold mb-4">Things other people work on</h2>
			<ul class="list-disc list-inside text-center">
				<li>Studying for Masters</li>
				<li>Learning to code</li>
				<li>Freelancing work</li>
				<li>Insert your project/goal here 😉</li>
			</ul>
		</div>

		<a href="https://connoradams.co.uk"
			><h2 class="text-3xl text-center font-semibold mb-4 text-blue-500 hover:text-blue-600">
				Contact me 📩
			</h2></a
		>

		<footer class="flex justify-center space-x-4 mt-8">
			<a href="https://connoradams.co.uk" class="text-blue-500 hover:text-blue-600">Home</a>
			<a href="https://www.linkedin.com" class="text-blue-500 hover:text-blue-600">LinkedIn</a>
			<a href="https://github.com" class="text-blue-500 hover:text-blue-600">GitHub</a>
			<a href="https://twitter.com" class="text-blue-500 hover:text-blue-600">Twitter</a>
			<a href="https://medium.com" class="text-blue-500 hover:text-blue-600">Medium</a>
			<a href="https://thepengestkhans.co.uk" class="text-blue-500 hover:text-blue-600">Location</a>
		</footer>
	</div>
</main>
