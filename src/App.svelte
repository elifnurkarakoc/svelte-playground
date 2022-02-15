<script>
  import User from "./components/User.svelte";
  import Form from "./components/Form.svelte";
  import Todos from "./components/Todos.svelte";
</script>

<div class="container">
  <h1>Svelte Playground</h1>
  <div class="wrapper">
    <div class="grid-item">
      <h2>Each Example</h2>
      {#each [0, 1, 2, 3] as number}
        <p>{number}</p>
      {/each}
    </div>
    <div class="grid-item">
      <User />
    </div>
    <div class="grid-item">
      <Form />
    </div>
    <div class="grid-item">
      <Todos />
    </div>
  </div>
</div>

<style>
  .container {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }
  .wrapper {
    display: grid;
    grid-template-columns: auto auto auto;
  }

  .grid-item {
    text-align: center;
  }
  @media (min-width: 640px) {
    .container {
      max-width: none;
    }
  }
</style>
