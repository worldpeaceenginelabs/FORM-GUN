<script lang="ts">

import Gun from "gun";

// declaring variables
var longitude: number; 
var latitude: number;

// Initialize GUN and tell it we will be storing all data under the key 'test'.
var gun = Gun(['https://gunrelayeurope.herokuapp.com/gun']).get('test')

// Fetch the input fields from form
async function handleSubmit(event) {
        console.log(event);
        console.log(event.target);

        //check if submit fills the values of the variables
        console.log(longitude)
        console.log(latitude)
        
        // Tell GUN to store an object
        gun.set({longitude, latitude});        
        
        // Show Gun data

        gun.on(data => console.log(data))
        }

</script>


<form on:submit|preventDefault="{handleSubmit}">
  <div>
    <label for="longitude">Longitude</label> 
    <input id="longitude" type="text" name="longitude" bind:value={longitude}>
    <br>
    <label for="latitude">Latitude</label>
    <input id="latitude" type="text" name="latitude" bind:value={latitude}>
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
