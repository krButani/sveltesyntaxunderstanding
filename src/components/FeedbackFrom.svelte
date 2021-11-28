<script>
  import Button from "./Button.svelte";
  import { createEventDispatcher } from "svelte";

  let text = ''; // you can bind control
  let dispatch = createEventDispatcher();


  const handleentername = () => {
    //let intext = document.getElementById('textgot').value; // similer you get value
    //console.log(intext);

    dispatch('changename',text);
  }

  const addcount = () => {
      dispatch('countchange');
  }
</script>

<div class="form-group">
  <form on:submit|preventDefault={handleentername}>
    <input type="text" id="textgot" placeholder="Enter Name" bind:value={text} />
    <br />
    <Button type="submit">Submit</Button> <Button on:click={addcount}>+ Add Count</Button>
  </form>
</div>

<style>
  .form-group {
    margin-top: 1rem;
  }
  input[type="text"] {
    padding: 0.6rem 0.75rem;
    border: none;
    border-radius: 5px;
  }
  input[type="text"]:focus {
    outline: none;
  }
</style>
