<script lang="ts">

import Gun from "gun";

// declaring variables
var name: any; 
var city: any; 

// Initialize GUN and tell it we will be storing all data under the key 'test'.
var gun = Gun(['https://gunrelayeurope.herokuapp.com/gun']).get('test')

// Fetch the input fields from form
async function handleSubmit(event) {
        console.log(event);
        console.log(event.target);

        //check if submit fills the values of the variables
        console.log(name)
        console.log(city)
        
        // Tell GUN to store an object
        gun.set({name, city});        
        
        gun.on(data => console.log(data))
        }

</script>


<form on:submit|preventDefault="{handleSubmit}">
  <div>
    <label for="name">Name</label> 
    <input id="name" type="text" name="name" bind:value={name}>
    <br>
    <label for="city">City</label>
    <input id="city" type="text" name="city" bind:value={city}>
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
