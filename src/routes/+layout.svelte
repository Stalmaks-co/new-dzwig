<script lang="ts">
	import Footer from '$lib/Footer.svelte';
	import Navbar from '$lib/Navbar.svelte';
	import '../app.css';

	let { children } = $props();
</script>

<Navbar />
{@render children()}
<Footer />
