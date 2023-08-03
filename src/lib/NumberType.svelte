<script lang="ts">
  let number: number = 0;
  $: console.log(number);
</script>

<div class="main">
  <input type="number" bind:value={number} />
  {#if number === 0 || number === 1}
    <p>number is one or zero</p>
  {:else if number % 2 === 0}
    <p>The number is even</p>
  {:else if number % 2 > 0}
    <p>is an odd number</p>
  {:else if number == null}
    <p>...</p>
  {/if}
</div>

<style>
  .main {
    text-align: center;
  }
  p {
    font-family: "Courier New", Courier, monospace;
    color: indigo;
  }
  input {
    height: 50px;
  }
</style>
