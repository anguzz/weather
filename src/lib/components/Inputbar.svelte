<script>
    export /**
* @type {any}
*/
     let value;
</script>

<input type="text" name="search" placeholder="Enter a city name" bind:value on:input autocomplete="off" />

<style> 

  input[type=text] {
      width: 35%;
      box-sizing: border-box;
      border: 1px solid rgb(204, 204, 204);
      border-bottom: 1px solid #ccc;
      font-size: 16px;
      background-color: none;
      background-position: 6px 6px; 
      background-repeat: no-repeat;
      padding: 8px 12px 8px 12px;
      outline: none;
      color:#1F2937;
      background-color:#6B91A4;
  }
  
  

</style>