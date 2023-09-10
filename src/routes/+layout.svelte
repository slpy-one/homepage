<script>
	import './main.css';

	import Navbar from '../lib/components/Navbar.svelte';
  import Footer from '../lib/components/Footer.svelte';
</script>

<div class="min-h-screen w-full bg-ctp-base text-ctp-text">
	<Navbar />
	<main>
		<slot />
	</main>
  <Footer />
</div>

<style>
	
</style>