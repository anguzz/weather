<script>
 import withQuery from "with-query"
 import Card from "$lib/components/Card.svelte";
 import Button from "$lib/components/Button.svelte";
 import Inputbar from "$lib/components/Inputbar.svelte";
 
 export let result = "";
 export let city = "";
  
 let searchitems = [];
 let url ="";
 const cache = new Map();

 async function handleSubmit(e) {
	e.preventDefault();
	
	url = withQuery('https://api.openweathermap.org/data/2.5/weather', {
		q: city,
		units: 'imperial',
		appid: '271d1234d3f497eed5b1d80a07b3fcd1', //YOUR_API_KEY
	 })

	if(cache.has(url)){
			alert("City already exists!")
	 } 
	else{
   
		await fetch(url)
			.then(resp => resp.json())
			.then(data => (result = data));

		const newSearchitem = {
			id: Math.random().toString(),
			city: result["name"],
			temp: result["main"]["temp"],
			icon: result["weather"][0]["icon"],
	     };

		searchitems = [...searchitems, newSearchitem];
		cache.set(url);
     }
}
</script>


<main>
	<form on:submit={handleSubmit}>
		<Inputbar bind:value={city} />
		<Button type="submit" caption="Search" />
	</form>
	<section id="searchitems">
		{#each searchitems as searchitem}
			<Card city={searchitem.city} temp={searchitem.temp} icon={searchitem.icon} />
		{/each}
	</section>
</main>

<style>
   section {
  
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 1rem;
  }

  @media (min-width: 768px) {
    section {
      grid-template-columns: repeat(6, 1fr);
    }
  }
</style>