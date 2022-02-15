<script>
  import { afterUpdate } from "svelte";
  export let todo;
</script>

<div on:click>
  {todo.text}
  {todo.done ? "👩🏼‍💻" : ""}
</div>
