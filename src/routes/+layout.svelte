<script>
	import './main.css';
  import Footer from '../lib/components/footer.svelte';
</script>

<div class="min-h-screen w-full bg-ctp-base text-ctp-text">
	<main>
		<slot />
	</main>
  <Footer />
</div>

<style>
	
</style>