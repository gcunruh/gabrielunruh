<script>
  import '../styles/tailwind-output.css';
  import Header from '../components/Header.svelte';
  import { page } from "$app/stores";
</script>

<main>
<Header page={$page}/>
<slot />
</main>
