<script>
	import Fa from 'svelte-fa';
	import { faPhone } from '@fortawesome/free-solid-svg-icons';
	import { goto } from '$app/navigation';
</script>

<section class="max-w-8xl px-2 py-8 sm:px-4 sm:py-12 lg:px-8">
	<div class="mx-auto w-full max-w-md sm:max-w-lg md:max-w-2xl rounded-lg bg-white p-4 sm:p-8 text-center shadow-lg">
		<h2 class="text-secondary mb-4 text-3xl xs:text-4xl sm:text-5xl md:text-6xl font-bold">Skontaktuj się z nami</h2>
		<p class="mb-6 text-base xs:text-lg sm:text-xl md:text-2xl text-gray-600">
			Jesteśmy gotowi odpowiedzieć na Twoje pytania i pomóc w wyborze najlepszego rozwiązania.
		</p>
		<button
			class="bg-accent mx-auto flex flex-row items-center justify-center rounded-md px-4 py-2 sm:px-6 sm:py-3 text-white text-base xs:text-lg sm:text-xl md:text-2xl transition duration-300 hover:bg-red-700 focus:outline-none focus:ring-2 focus:ring-red-500 focus:ring-offset-2"
			on:click={() => goto('/kontakt')}
			>
			<p>Skontaktuj się</p>
			<Fa icon={faPhone} class="ml-2 text-base xs:text-lg sm:text-xl" />
		</button>
	</div>
</section>
