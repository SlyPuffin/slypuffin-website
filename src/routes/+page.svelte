<script>
  import { goto } from '$app/navigation';

  function handleClick(route) {
    goto(route);
  }
</script>
<style>
  button {
    cursor: pointer;
  }
 img {
    max-width: 100%;
    height: auto;
  }
</style>

<main>
  <button on:click={() => handleClick('/programming')}>
    <img src="/Puffin-Nest-Icon.png" alt="Nest Building">
  </button>
  <button on:click={() => handleClick('/art')}>
    <img src="/Puffin-Call-Icon.png" alt="Bird Calls">
  </button>
  <button on:click={() => handleClick('/blog')}>
    <img src="/Puffin-Fish-Icon.png" alt="Hunts">
  </button>
</main>

