<script>
  import Todo from "./Todo.svelte";
  let todos = [
    {
      id: 1,
      done: true,
      text: "Todo 1",
    },
    {
      id: 2,
      done: true,
      text: "Todo 2",
    },
    {
      id: 3,
      done: false,
      text: "Todo 3",
    },
  ];

  const toggle = (id) => {
    todos = todos.map((todo) => {
      if (todo.id === id) {
        return {
          id,
          done: !todo.done,
          text: todo.text,
        };
      }
      return todo;
    });
  };
</script>

<div>
  <h2>Todo Example</h2>
  {#each todos as todo}
    <Todo {todo} on:click={() => toggle(todo.id)} />
  {/each}
</div>
