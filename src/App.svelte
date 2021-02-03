<script lang="ts">
  import Search from './components/search/Search.svelte';

  const handleSubmit = (event: CustomEvent<string>) => {
    console.log(event.detail)
  }
</script>

<main>
  <Search on:submit={handleSubmit} />
</main>

<style>

</style>