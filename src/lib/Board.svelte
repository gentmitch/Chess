<script>
  import Square from './Square.svelte';
  let board = [];

  for (let file = 0; file < 8; file++) {
    for (let rank = 0; rank < 8; rank++) {
      board.push(file + rank);
    }
  }
</script>

<div>
  {#each board as i}
    {#if i % 2 !== 0}
      <Square color={0}></Square>
    {:else}
    <Square color={1}></Square>
    {/if}
  {/each}
</div>

<style>
  div {
    display: grid;
    grid-template-columns: repeat(8, 60px);
    grid-template-rows: repeat(8, 60px);
  }
</style>