<script lang="ts">
  import '../app.css';
  import Header from '$lib/Header.svelte';
  import Footer from '../lib/Footer.svelte';
  import "lucide";
  const { children } = $props();
</script>


<Header />
<main>
{@render children()}
</main>

<Footer />
