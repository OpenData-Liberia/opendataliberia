<script lang="ts">
  import '../app.css';
  import Header from '$lib/Header.svelte';
  import Footer from '../lib/Footer.svelte';
  const { children } = $props();
</script>

<Header />
<main>
{@render children()}
</main>

<Footer />
