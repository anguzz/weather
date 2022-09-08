<script>
    export /**
* @type {any}
*/
     let value;
</script>

<input type="text" name="search" placeholder="Enter city name here" bind:value on:input />

<style> 

  input[type=text] {
      width: 35%;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-bottom: 1px solid #ccc;
      font-size: 16px;
      background-color: none;
      background-position: 6px 6px; 
      background-repeat: no-repeat;
      padding: 8px 12px 8px 12px;
      outline: none;
  }

</style>