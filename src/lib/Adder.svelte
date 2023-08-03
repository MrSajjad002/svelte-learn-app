<script lang="ts">
  let numbers: number[] = [0];

  const adder = () => {
    numbers = [...numbers, numbers.length + 1];
  };

  $: sum = numbers.reduce((acc, number) => acc + number, 0);
</script>

<div class="main">
  <p>{numbers.join("+")} = {sum}</p>
  <button type="button" on:click={adder}>add</button>
</div>

<style>
  .main {
    text-align: center;
    margin: 2rem;
  }
  p {
    font-family: "Courier New", Courier, monospace;
    color: darkcyan;
  }
  button {
    border-radius: 16px;
    background: #f7ae10;
    padding: 20px;
    width: 150px;
    height: 60px;
    font-family: "Courier New", Courier, monospace;
    font-weight: bold;
    font-size: medium;
  }
</style>
