<script>
	import Fa from 'svelte-fa';
	import { faXmark } from '@fortawesome/free-solid-svg-icons';
	export let title = '';
</script>

<div class="bg-opacity-50 fixed inset-0 z-50 flex items-center justify-center bg-black/75">
	<div class="w-full max-w-2xl rounded-lg bg-white p-6 shadow-lg">
		<div class="mb-4 flex flex-row items-center justify-between">
			<h2 class="text-xl font-semibold">{title}</h2>
			<button on:click class="cursor-pointer text-gray-500 hover:text-gray-700 focus:outline-none">
				<Fa icon={faXmark} class="text-xl" />
			</button>
		</div>
		<slot></slot>
	</div>
</div>
