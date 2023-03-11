<script>
  import ExpandableItem from './ExpandableItem.svelte';
  export let items;
</script>

{#each items as item}
  <ExpandableItem title={item.title} links={item.links} />
{/each}

