<script lang="ts">

import Gun from "gun";

// Fetch the input fields from form
async function handleSubmit(event) {
        console.log(event);
        console.log(event.target);
        console.log(event.target.name.value);
        console.log(event.target.city.value);
        console.log(name)
        console.log(city)
        
        // initialize Gun
        const gun = Gun(['https://gunrelayeurope.herokuapp.com/gun'])
        
        const create = () => gun.get("test").put({name}).put({city})
        console.log(gun)
        }
 
 //
 let name = ""
 let city = ""
 
</script>



<form on:submit|preventDefault="{handleSubmit}">
  <div>
    <label for="name">Name</label>
    <input id="name" type="text" name="name" bind:value={name}>
    <br>
    <label for="city">City</label>
    <input id="city" type="text" name="city"bind:value={city}>
  </div>

  <div>
    <input type="submit" value="Send">
  </div>
</form>



<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }
</style>
