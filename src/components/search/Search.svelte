<script lang="ts">
  import { createEventDispatcher } from 'svelte';

  let searchTerm: string = '';
  const dispatchSubmit = createEventDispatcher();

  const handleSubmit = () => {
    dispatchSubmit('submit', searchTerm)
  }
</script>

<form on:submit|preventDefault={handleSubmit}>
  <input placeholder="Search" bind:value={searchTerm} name="search" />
  <input type="submit" value="Search" />
</form>

<style>

</style>