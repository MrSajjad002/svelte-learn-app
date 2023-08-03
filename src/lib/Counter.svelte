<script lang="ts">
  let count: number = 0;
  $: double = count * 2;
  const plus = () => {
    count++;
  };

  $: {
    console.log(`count cheng to ${count} an double is ${double}`);
  }
</script>

<div class="board">
  <h1>counter</h1>
  <button type="button" on:click={plus}>
    <span>count {count}</span>
  </button>

  <p>double count is {double}</p>
</div>

<style>
  .board {
    text-align: center;
    margin-top: 50px;
    font-family: "Courier New", Courier, monospace;
  }

  button {
    border-radius: 16px;
    background: #73ad21;
    padding: 20px;
    width: 150px;
    height: 60px;
    font-family: "Courier New", Courier, monospace;
    font-weight: bold;
    font-size: medium;
  }
</style>
