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
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
    border-radius: 5px;
    background: #6B91A4;
    margin: 1.5rem;
    height: 14rem;
    text-align: center;
  }

  .image {
    width: 100%;
    height: 10rem;
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

 
  h2 {
    font-size: 1rem;
    color: #1F2937;
  }


</style>

