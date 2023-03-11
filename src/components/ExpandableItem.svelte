<script>
  export let title;
  export let links;
  
  let expanded = false;
  
  function toggleExpanded() {
    expanded = !expanded;
  }
</script>

<div class="item">
  <h2 on:click={toggleExpanded}>{title}</h2>
  
  {#if expanded}
    <ul>
      {#each links as link}
        <li><a href={link.href}>{link.text}</a></li>
      {/each}
    </ul>
  {/if}
</div>

<style>
  .item {
    margin-bottom: 1rem;
  }
  
  h2 {
    cursor: pointer;
  }
  
  ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  li {
    margin: 0.5rem 0;
  }
</style>

