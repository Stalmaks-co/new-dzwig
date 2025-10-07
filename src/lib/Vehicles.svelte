<script lang="ts">
	import { goto } from '$app/navigation';
	import {
		faMagnifyingGlass,
		faShoppingBasket,
		faArrowUpRightFromSquare,
		faXmark
	} from '@fortawesome/free-solid-svg-icons';
	import Fa from 'svelte-fa';
	import Modal from './Modal.svelte';

	const handleClickSteel = () => {
		window.location.href = 'https://stalmaks.pl';
	};

	let modal = {
		title: '',
		shown: false,
		prop: ''
	};

	const handleMoreInfo = (name: string, prop: string) => {
		modal.title = name;
		modal.shown = true;
		modal.prop = prop;
	};

	const handleCloseModal = () => {
		modal.shown = false;
	};
</script>

<section
	class="mx-auto max-w-[90rem] space-y-10 px-2 py-6 sm:px-4 sm:py-8 lg:px-8 2xl:max-w-[95rem]"
>
	<div class="flex flex-col items-center justify-center">
		<h2
			class="border-accent xs:text-5xl mb-2 scroll-m-22 border-b-4 pb-4 text-center text-4xl font-bold sm:text-6xl md:text-7xl"
			id="services"
		>
			Nasze maszyny
		</h2>
	</div>
	<article class="grid grid-cols-1 gap-6 md:grid-cols-2">
		<div
			class="flex min-h-[420px] w-full flex-col justify-center overflow-hidden rounded-b-lg shadow-lg sm:min-h-[380px]"
		>
			<img src="./vehicles/dzwig.webp" alt="Dźwig 1" class="w-full rounded-t-lg object-cover" />
			<div class="text-secondary xs:p-4 flex h-fit flex-col justify-between bg-white p-3 xl:h-1/3">
				<div>
					<h3 class="xs:text-2xl text-xl font-semibold sm:text-3xl">Dźwig Liebherr LTM 1030</h3>
					<p class="xs:text-base text-sm sm:text-lg">
						Dźwig Liebherr LTM 1030 pozwala na transport ładunków o maksymalnej masie do 30 ton.
						Wysięgnik podstawowy dźwigu samojezdnego mierzy 30 m, a wysięgnik pomocniczy 8 m. Łączna
						maksymalna wysokość podnoszenia 38 m.a
					</p>
				</div>
				<div class="flex flex-row items-center gap-2">
					<button
						class="bg-accent border-accent xs:px-4 mt-2 flex w-fit cursor-pointer flex-row items-center justify-center rounded-lg border-2 px-3 py-2 text-white transition duration-200 hover:bg-red-700 focus:ring-2 focus:ring-red-500 focus:ring-offset-2 focus:outline-none sm:px-4 sm:py-2"
						onclick={() => {
							goto('/kontakt');
						}}
					>
						<p class="xs:text-lg mr-2 text-base sm:text-xl">Zamów</p>
						<Fa icon={faShoppingBasket} class="xs:text-base inline-block text-sm sm:text-lg" />
					</button>
					<button
						class="border-accent text-accent xs:px-4 mt-2 flex w-fit cursor-pointer flex-row items-center justify-center rounded-lg border-2 px-3 py-2 transition duration-200 focus:ring-2 focus:ring-red-500 focus:ring-offset-2 focus:outline-none sm:px-4 sm:py-2"
						onclick={() => handleMoreInfo('Dźwig Liebherr LTM 1030', 'dzwig')}
					>
						<p class="xs:text-lg mr-2 text-base sm:text-xl">Więcej informacji</p>
						<Fa icon={faMagnifyingGlass} class="xs:text-base inline-block text-sm sm:text-lg" />
					</button>
				</div>
			</div>
		</div>
		<div
			class="flex min-h-[420px] w-full flex-col justify-center overflow-hidden rounded-b-lg shadow-lg sm:min-h-[380px]"
		>
			<img src="./vehicles/ladowarka.webp" alt="Dźwig 1" class="w-full rounded-t-lg object-cover" />
			<div class="text-secondary xs:p-4 flex h-fit flex-col justify-between bg-white p-3 xl:h-1/3">
				<div>
					<h3 class="xs:text-2xl text-xl font-semibold sm:text-3xl">
						Ładowarka Teleskopowa Komatsu WH714H
					</h3>
					<p class="xs:text-base text-sm sm:text-lg">
						Maszyna WH714H należy zapewnia 14 metrów wysokości podniesienia, 4.5T udźwigu, 10m
						maksymalnego zasięgu, duży rozstaw osi, blokada tylnej osi<br />
					</p>
				</div>
				<div class="flex flex-row items-center gap-2">
					<button
						class="bg-accent border-accent xs:px-4 mt-2 flex w-fit cursor-pointer flex-row items-center justify-center rounded-lg border-2 px-3 py-2 text-white transition duration-200 hover:bg-red-700 focus:ring-2 focus:ring-red-500 focus:ring-offset-2 focus:outline-none sm:px-4 sm:py-2"
						onclick={() => {
							goto('/kontakt');
						}}
					>
						<p class="xs:text-lg mr-2 text-base sm:text-xl">Zamów</p>
						<Fa icon={faShoppingBasket} class="xs:text-base inline-block text-sm sm:text-lg" />
					</button>
					<button
						class="border-accent text-accent xs:px-4 mt-2 flex w-fit cursor-pointer flex-row items-center justify-center rounded-lg border-2 px-3 py-2 transition duration-200 focus:ring-2 focus:ring-red-500 focus:ring-offset-2 focus:outline-none sm:px-4 sm:py-2"
						onclick={() => handleMoreInfo('Ładowarka Teleskopowa Komatsu WH714H', 'ladowarka')}
					>
						<p class="xs:text-lg mr-2 text-base sm:text-xl">Więcej informacji</p>
						<Fa icon={faMagnifyingGlass} class="xs:text-base inline-block text-sm sm:text-lg" />
					</button>
				</div>
			</div>
		</div>
		<div
			class="flex min-h-[420px] w-full flex-col justify-center overflow-hidden rounded-b-lg shadow-lg sm:min-h-[380px]"
		>
			<img src="./vehicles/podnosnik.webp" alt="Dźwig 1" class="w-full rounded-t-lg object-cover" />
			<div class="text-secondary xs:p-4 flex h-fit flex-col justify-between bg-white p-3 xl:h-1/3">
				<div>
					<h3 class="xs:text-2xl text-xl font-semibold sm:text-3xl">Podnośnik przegubowy E450AJ</h3>
					<p class="xs:text-base text-sm sm:text-lg">
						Podest przegubowy elektryczny JLG E450AJ. Podnośnik zapewnia 15,72 m wysokości roboczej
						i 7,24 m wysięgu bocznego. Zwyżki o udźwigu 230 kg, przeznaczone do pracy 2 operatorów w
						koszu.
					</p>
				</div>
				<div class="flex flex-row items-center gap-2">
					<button
						class="bg-accent border-accent xs:px-4 mt-2 flex w-fit cursor-pointer flex-row items-center justify-center rounded-lg border-2 px-3 py-2 text-white transition duration-200 hover:bg-red-700 focus:ring-2 focus:ring-red-500 focus:ring-offset-2 focus:outline-none sm:px-4 sm:py-2"
						onclick={() => {
							goto('/kontakt');
						}}
					>
						<p class="xs:text-lg mr-2 text-base sm:text-xl">Zamów</p>
						<Fa icon={faShoppingBasket} class="xs:text-base inline-block text-sm sm:text-lg" />
					</button>
					<button
						class="border-accent text-accent xs:px-4 mt-2 flex w-fit cursor-pointer flex-row items-center justify-center rounded-lg border-2 px-3 py-2 transition duration-200 focus:ring-2 focus:ring-red-500 focus:ring-offset-2 focus:outline-none sm:px-4 sm:py-2"
						onclick={() => handleMoreInfo('Podnośnik przegubowy E450AJ', 'podnosnik')}
					>
						<p class="xs:text-lg mr-2 text-base sm:text-xl">Więcej informacji</p>
						<Fa icon={faMagnifyingGlass} class="xs:text-base inline-block text-sm sm:text-lg" />
					</button>
				</div>
			</div>
		</div>
		<div
			class="flex min-h-[420px] w-full flex-col justify-center overflow-hidden rounded-b-lg shadow-lg sm:min-h-[380px]"
		>
			<img src="./vehicles/spawacz.webp" alt="Dźwig 1" class="w-full rounded-t-lg object-cover" />
			<div class="text-secondary xs:p-4 flex h-fit flex-col justify-between bg-white p-3 xl:h-1/3">
				<div>
					<h3 class="xs:text-2xl text-xl font-semibold sm:text-3xl">Konstrukcje stalowe</h3>
					<ul class="xs:pl-6 xs:text-base list-disc pl-4 text-sm sm:text-lg">
						<li>słupy, estakady, podesty, przejścia BHP</li>
						<li>stojaki, stoły, urządzenia przemysłowe</li>
						<li>ogrodzenia, przesuwne bramy wjazdowe</li>
					</ul>
				</div>
				<div class="flex flex-row items-center gap-2">
					<button
						class="bg-accent border-accent xs:px-4 mt-2 flex w-fit cursor-pointer flex-row items-center justify-center rounded-lg border-2 px-3 py-2 text-white transition duration-200 hover:bg-red-700 focus:ring-2 focus:ring-red-500 focus:ring-offset-2 focus:outline-none sm:px-4 sm:py-2"
						onclick={handleClickSteel}
					>
						<p class="xs:text-lg mr-2 text-base sm:text-xl">Przejdź</p>
						<Fa
							icon={faArrowUpRightFromSquare}
							class="xs:text-base inline-block text-sm sm:text-lg"
						/>
					</button>
				</div>
			</div>
		</div>
	</article>

	{#if modal.shown}
		{#if modal.prop === 'dzwig'}
			<Modal title={modal.title} on:click={handleCloseModal}>
				<div class="mx-auto flex flex-col">
					<div class="grid grid-cols-2 gap-2">
						<img
							src="./vehicles/dzwig/dzwig1.webp"
							alt="Dźwig Liebherr LTM 1030"
							class="mt-28 h-[55%] rotate-90 rounded-lg object-cover"
						/>
						<img
							src="./vehicles/dzwig/dzwig2.webp"
							alt="Dźwig Liebherr LTM 1030"
							class="w-full rounded-lg object-cover"
						/>
					</div>

					<p class="text-secondary xs:text-base mt-4 text-sm sm:text-lg">
						Dźwig Liebherr LTM 1030 pozwala na transport ładunków o maksymalnej masie do 30 ton.
						Wysięgnik podstawowy dźwigu samojezdnego mierzy 30 m, a wysięgnik pomocniczy 8 m. Łączna
						maksymalna wysokość podnoszenia zapewniana przez dźwig Liebherr LTM 1030 wynosi 38 m.
					</p>
				</div>
				<div class="flex flex-row items-center gap-4">
					<button
						class="bg-accent border-accent xs:px-4 mt-2 flex w-fit cursor-pointer flex-row items-center justify-center rounded-lg border-2 px-3 py-2 text-white transition duration-200 hover:bg-red-700 focus:ring-2 focus:ring-red-500 focus:ring-offset-2 focus:outline-none sm:px-4 sm:py-2"
						onclick={() => {
							goto('/kontakt');
						}}
					>
						<p class="xs:text-lg mr-2 text-base sm:text-xl">Zamów</p>
						<Fa icon={faShoppingBasket} class="xs:text-base inline-block text-sm sm:text-lg" />
					</button>
					<button
						class="border-accent text-accent xs:px-4 mt-2 flex w-fit cursor-pointer flex-row items-center justify-center rounded-lg border-2 px-3 py-2 transition duration-200 focus:ring-2 focus:ring-red-500 focus:ring-offset-2 focus:outline-none sm:px-4 sm:py-2"
						onclick={handleCloseModal}
					>
						<p class="xs:text-lg mr-2 text-base sm:text-xl">Zamknij</p>
						<Fa icon={faXmark} class="xs:text-base inline-block text-sm sm:text-lg" />
					</button>
				</div>
			</Modal>
		{:else if modal.prop === 'ladowarka'}
			<Modal title={modal.title} on:click={handleCloseModal}>
				<div class="flex flex-col">
					<div class="grid grid-cols-2 gap-2">
						<img
							src="./vehicles/ladowarka/ladowarka1.webp"
							alt="Ładowarka Teleskopowa Komatsu WH714H"
							class="w-full rounded-lg object-cover"
						/>
						<img
							src="./vehicles/ladowarka/ladowarka2.webp"
							alt="Ładowarka Teleskopowa Komatsu WH714H"
							class="w-full rounded-lg object-cover"
						/>
					</div>
					<p class="text-secondary xs:text-base mt-4 text-sm sm:text-lg">
						Wysokość robocza: 15.72 m <br /> Wysięg roboczy: 7.89 m <br /> Udźwig platformy: 230 kg
						<br />
						Możliwość doboru z czterech modeli z wysokością roboczą do 15,50 m i różnych opcji zwiększa
						uniwersalność Automatyczna kontrola trakcji w standardzie zwiększa wydajność w terenie i
						możliwości manewrowania Wysoko wydajny, bezpośredni napęd elektryczny z dłuższymi cyklami
						pracy zwiększa produktywność Zerowa emisja zanieczyszczeń do środowiska sprawia, że podnośniki
						są przyjazne dla środowiska
					</p>
				</div>
				<div class="flex flex-row items-center gap-4">
					<button
						class="bg-accent border-accent xs:px-4 mt-2 flex w-fit cursor-pointer flex-row items-center justify-center rounded-lg border-2 px-3 py-2 text-white transition duration-200 hover:bg-red-700 focus:ring-2 focus:ring-red-500 focus:ring-offset-2 focus:outline-none sm:px-4 sm:py-2"
						onclick={() => {
							goto('/kontakt');
						}}
					>
						<p class="xs:text-lg mr-2 text-base sm:text-xl">Zamów</p>
						<Fa icon={faShoppingBasket} class="xs:text-base inline-block text-sm sm:text-lg" />
					</button>
					<button
						class="border-accent text-accent xs:px-4 mt-2 flex w-fit cursor-pointer flex-row items-center justify-center rounded-lg border-2 px-3 py-2 transition duration-200 focus:ring-2 focus:ring-red-500 focus:ring-offset-2 focus:outline-none sm:px-4 sm:py-2"
						onclick={handleCloseModal}
					>
						<p class="xs:text-lg mr-2 text-base sm:text-xl">Zamknij</p>
						<Fa icon={faXmark} class="xs:text-base inline-block text-sm sm:text-lg" />
					</button>
				</div>
			</Modal>
		{:else if modal.prop === 'podnosnik'}
			<Modal title={modal.title} on:click={handleCloseModal}>
				<div class="flex flex-col">
					<div class="grid grid-cols-2 gap-2">
						<img
							src="./vehicles/podnosnik/podnosnik1.webp"
							alt="Podnośnik przegubowy E450AJ"
							class="w-full rounded-lg object-cover"
						/>
						<img
							src="./vehicles/podnosnik/podnosnik2.webp"
							alt="Podnośnik przegubowy E450AJ"
							class="w-full rounded-lg object-cover"
						/>
					</div>
					<p class="text-secondary xs:text-base mt-4 text-sm sm:text-lg">
						WYSOKOŚĆ PODNOSZENIA: 14.100 mm <br />
						UDŹWIG: 4.500 kg <br />
						MASA W STANIE GOTOWYM DO PRACY: 11.180 kg <br />
						Specjalny kształt ramy pozwolił umieścić przegub wysięgnika najniżej wśród maszyn dostępnych
						na rynku. Niskoprofilowy wysięgnik Super Low Boom Profile zapewnia wyjątkową stabilność i
						widoczność. W przypadku ładowarek teleskopowych te dwie cechy są najważniejsze.
					</p>
				</div>
				<div class="flex flex-row items-center gap-4">
					<button
						class="bg-accent border-accent xs:px-4 mt-2 flex w-fit cursor-pointer flex-row items-center justify-center rounded-lg border-2 px-3 py-2 text-white transition duration-200 hover:bg-red-700 focus:ring-2 focus:ring-red-500 focus:ring-offset-2 focus:outline-none sm:px-4 sm:py-2"
						onclick={() => {
							goto('/kontakt');
						}}
					>
						<p class="xs:text-lg mr-2 text-base sm:text-xl">Zamów</p>
						<Fa icon={faShoppingBasket} class="xs:text-base inline-block text-sm sm:text-lg" />
					</button>
					<button
						class="border-accent text-accent xs:px-4 mt-2 flex w-fit cursor-pointer flex-row items-center justify-center rounded-lg border-2 px-3 py-2 transition duration-200 focus:ring-2 focus:ring-red-500 focus:ring-offset-2 focus:outline-none sm:px-4 sm:py-2"
						onclick={handleCloseModal}
					>
						<p class="xs:text-lg mr-2 text-base sm:text-xl">Zamknij</p>
						<Fa icon={faXmark} class="xs:text-base inline-block text-sm sm:text-lg" />
					</button>
				</div>
			</Modal>
		{/if}
	{/if}
</section>

<svelte:window
	on:keydown={(e) => {
		if (e.key === 'Escape' && modal.shown) {
			handleCloseModal();
		}
	}}
/>
