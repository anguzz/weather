<script>
 import withQuery from "with-query"
 import Card from "$lib/components/Card.svelte";
 import Button from "$lib/components/Button.svelte";
 import Inputbar from "$lib/components/Inputbar.svelte";
 import Text from "$lib/components/Text.svelte";
 import Anchor from "$lib/components/Anchor.svelte";
 export let result = "";
 export let city = "";
  
 /**
* @type {any[]}
*/
 let searchitems = [];
 let url ="";
 const cache = new Map();

 /**
* @param {{ preventDefault: () => void; }} e
*/
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
			// @ts-ignore
			city: result["name"],
			// @ts-ignore
			temp: result["main"]["temp"],
			// @ts-ignore
			icon: result["weather"][0]["icon"],
	     };

		searchitems = [...searchitems, newSearchitem];
		// @ts-ignore
		cache.set(url);
     }
}
</script>
<Anchor id="search" />
<div id="bg">

	<Text>
		
		
	<form on:submit={handleSubmit}>
		<Inputbar bind:value={city} />
		<Button type="submit" caption="Search" />
	</form>
</Text>


	<section id="searchitems">
		{#each searchitems as searchitem}
			<Card city={searchitem.city} temp={searchitem.temp} icon={searchitem.icon} />
		{/each}
	</section>


</div>

<style>
	  #bg {
  background-color: rgb(68, 68, 116);
  padding-top:5rem;
  height: 100vh; 
  }
   section {
   color:rgb(28, 83, 125);
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