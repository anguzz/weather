<script>
    export /**
* @type {any}
*/
     let city;
    export /**
* @type {any}
*/
     let temp;
    export /**
* @type {any}
*/
     let icon;
</script>

<card>
    <h1>{city}</h1>
    <h2>{temp} ° F</h2>
    <div class="image">
        <img src="https://openweathermap.org/img/w/{icon}.png" alt="weathericon">
    </div>
</card>


<style>
  card {
    box-shadow: 0 2px 8px #161925;
    border-radius: 5px;
    background: #161925;
    margin: 1.5rem;
    height: 10rem;
    text-align: center;
    -webkit-touch-callout: none; /* iOS Safari */
    -webkit-user-select: none; /* Safari */
     -khtml-user-select: none; /* Konqueror HTML */
       -moz-user-select: none; /* Old versions of Firefox */
        -ms-user-select: none; /* Internet Explorer/Edge */
            user-select: none;

  }

  .image {
    width: 50%;
    height: 5rem;
  }

  .image img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }

  h1 {
    font-size: 1.25rem;
    margin: 1rem 0;
    font-family: "Roboto Slab", sans-serif;
  }

 h1{
  color: #ffffff;

 }
  h2 {
    font-size: 1rem;
    color: #ffffff;
  }


</style>

