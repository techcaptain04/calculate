<!-- create a calculator using svelte -->
<script lang="ts">
  import Gosling from "./Gosling.svelte";
  import Pixies from "./Pixies.svelte";

  let num1 = 0;
  let num2 = 0;
  let result = 0;
  let changed = false;
  
  $:if (result) {
    changed = true;
  }
  function add() {
    result = num1 + num2;
  }

  function subtract() {
    result = num1 - num2;
  }

  function multiply() {
    result = num1 * num2;
  }

  function divide() {
    result = num1 / num2;
  }
</script>
<style scoped>
  .calculator {
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 100vh;
  }
  .inputs {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
  }

  .buttons {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
    margin-bottom: 1rem;
  }
</style>

<div class="calculator">
  <h1>Calculator</h1>
  
  <class class="inputs">
    <input type="number" bind:value={num1} />
    <input type="number" bind:value={num2} />
  
  </class>
  
  <div class="buttons">
    <button on:click={add}>Add</button>
    <button on:click={subtract}>Subtract</button>
    <button on:click={multiply}>Multiply</button>
    <button on:click={divide}>Divide</button>
  
  </div>
  {#if changed}
    <Gosling result={result} />

  {:else}
    <h2>Result: {result}</h2>
  {/if}

  <Pixies isPlaying={changed} />
</div>
