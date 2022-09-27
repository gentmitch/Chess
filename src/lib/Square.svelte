<script>
  export let color = 0;
</script>


<div class:dark={color === 0} class:light={color ===1}></div>

<style>
  div {
    width: 64px;
    height: 64px;
  }
  .dark {
    background-color: rgb(134, 103, 103);
  }
  .light {
    background-color: #bebebe;
  }
</style>