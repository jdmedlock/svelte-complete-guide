<script>
  let userPassword = ''
  let passwords = []

  const addPassword = () => {
    passwords = [...passwords, userPassword]
    userPassword = ''
  }

  const removePassword = (event) => {
    const passwordIndex = passwords.indexOf(event.target.innerText)
    passwords.splice(passwordIndex, 1)
    passwords = passwords
  }
</script>

<div id="form">
  <label for="password">Password:</label>
  <input id="password" type="text" bind:value="{ userPassword }" />

  <div class="errorMsg">
    {#if userPassword.length < 5}
      Too short (must be between 5 and 10 characters)
    {:else if userPassword.length > 10}
      Too long (must be between 5 and 10 characters)
    {/if}
  </div>

  {#if userPassword.length >= 5 && userPassword.length <= 10}
    <p>{ userPassword }</p>
    <button on:click="{ addPassword }">Add password</button>
  {/if}

  <ul>
  {#each passwords as password, i (password)}
    <li on:click="{ removePassword }">{ password }</li>
  {/each}
  </ul>

</div>


<style>
  #form {
    background-color: #FFF;
    height: auto;
    width: 750px;
    margin-top: 0px;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    padding: 0px;
  }
  label {
      font-size: 20px;
      color: white;
      background-color: rgb(39, 119, 205);
      height: 24px;
      margin-left: 10px;
      margin-right: 5px;
      float:left;
  }
  input {
      height: 24px;
      width: 150;
      border: 1px solid #000;
  }

  .errorMsg {
    color: red;
    height: 24px;
    font-size: 20px;
    float: right;
  }

  button {
    color: white;
    background-color: teal;
    border-radius: 10px;
    font-size: 20px;
  }
</style>