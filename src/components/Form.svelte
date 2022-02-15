<script>
  $: users = [
    { name: "elif", surname: "karakoc", username: "elifkarakoc" },
    { name: "nur", surname: "karakoc", username: "nurkarakoc" },
  ];

  let name = "";
  let surname = "";
  let username = "";

  const add = () => {
    users = users.concat({ name, surname, username });
  };
</script>

<div>
  <h2>Form Example</h2>
  <div>
    <div>
      <input bind:value={username} type="text" placeholder="Username" />
    </div>
    <div>
      <input bind:value={name} type="text" placeholder="Name" />
    </div>
    <div>
      <input bind:value={surname} type="text" placeholder="Surname" />
    </div>
  </div>
  <div>
    <button on:click={add}>Add</button>
  </div>
  <div>
    <br />
    <div>username - name surname</div>
    {#each users as user, i}
      <p key={i}>{user.username} - {user.name} {user.surname}</p>
    {/each}
  </div>
</div>
