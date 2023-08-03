<script lang="ts">
  import Adder from "./lib/Adder.svelte";
  import Counter from "./lib/Counter.svelte";
  import Message from "./lib/Message.svelte";

  const text = "svelte";
</script>

<h1>{text}</h1>
<Message text={"Welcome to svelte tutorial 😊"} />
<hr class="line" />
<Counter />
<hr class="line" />
<Adder />

<style>
  h1 {
    font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
    color: rgb(243, 79, 33);
  }
  .line {
    width: 500px;
    margin-top: 20px;
  }
</style>
