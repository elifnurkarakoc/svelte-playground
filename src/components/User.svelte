<script>
  import { onMount } from "svelte";
  let user;
  onMount(async () => {
    user = await fetch("https://jsonplaceholder.typicode.com/users/1").then(
      (x) => x.json()
    );
  });
</script>

<div>
  <h2>Fetch Example</h2>
  <p>User Id: {user?.id}</p>
  <p>UserName: {user?.username}</p>
  <p>Email: {user?.email}</p>
</div>
