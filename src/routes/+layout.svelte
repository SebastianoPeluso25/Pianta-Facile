<script>
    import { onMount } from "svelte";
    import Item from "../lib/components/item.svelte";
    import Noresult from "../lib/components/noresult.svelte";
    import Search from "../lib/components/search.svelte";
    import Menu from "../lib/components/menu.svelte";
    import Nav from "../lib/components/nav.svelte";
    import Footer from "../lib/components/footer.svelte";

    import {data} from "../lib/js/data.js";

    let filteredCards = [];
    let tags = []; 
    let selectedtag = "";


    const getLanguages = () => {
		for (let cardObj of data) {
			if (!tags.includes(cardObj.mese)) {
				tags = [...tags, cardObj.mese]
			}
		}
		tags = tags.sort();
	}	
	onMount(() => getLanguages());
	
	// For Select Menu
	$: if (selectedtag) getCardsByLang();
	$: console.log(filteredCards, selectedtag);
	
	const getCardsByLang = () => {
		
		searchTerm = ""; 
		
		if (selectedtag === "all") {
			return filteredCards = [];
		} 
		return filteredCards = data.filter(card => card.mese === selectedtag);

	}	

    let searchTerm = "";
	
	$: if (searchTerm) selectedtag = "";
	
	const searchcards = () => {	
		return filteredCards = data.filter(card => {
			let cardTitle = card.title.toLowerCase();
			return cardTitle.includes(searchTerm.toLowerCase())
		});
	}

</script>

<Nav />

<div class="search_container">
    <Search bind:searchTerm on:input={searchcards} />
    <Menu {tags} bind:selectedtag  />
</div>

<div class="container">
    <div class="top">
        
        <div class="card" name="card">
            {#if searchTerm && filteredCards.length === 0}
            <Noresult />	
        {:else if filteredCards.length > 0}
            {#each filteredCards as {tag,link,img, title, description}}
                <Item {tag} {link} {img} {title} {description}/>
            {/each}	
        {:else}
            {#each data as {tag, link, img, title, description}}
                <Item  {tag} {link} {img} {title} {description} />
            {/each}	
        {/if}
        </div>
    </div>

    <div class="bottom">
       <slot /> 
    </div>
</div>


<Footer />

<style>

@media(min-width:480px){

.search_container{
    width: 50%;
    margin: auto;
    margin-top: 4%;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    box-shadow: 1px 1px 6px 2px #e85d04;
    padding: 20px;
    background-color: #e85d04;
}

.container{
    width: 80%;
    margin: 8vh auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    justify-items: center;
    row-gap: 20px;
    
    
    
}

:global(::selection){
    
    background-color: #9ef1d9;
}


.container > .top{
    display: flex;
    align-items: center;
    width: 100%;
    height: 300px;
    margin: auto;
    overflow: auto;
    white-space: nowrap;
   
    
    
}

.top > .card{
    display: flex;
    flex-direction: row;
    column-gap: 20px;
    padding: 10px;
    
}


.container > .bottom{
        border-radius: 10px;
		box-shadow: 1px 1px 6px 2px #1DD59E;
        padding: 36px;
        
        
    }





}


@media(max-width:480px){

.search_container{
    width: 80%;
    margin: auto;
    margin-top: 4%;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    box-shadow: 1px 1px 6px 2px #e85d04;
    padding: 20px;
    background-color: #e85d04;
}

.container{
    width: 80%;
    margin: 8vh auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    justify-items: center;
    
    
    
}

:global(::selection){
    
    background-color: #9ef1d9;
}


.container > .top{
    display: flex;
    align-items: center;
    width: 100%;
    height: 300px;
    margin: auto;
    overflow: auto;
    white-space: nowrap;
   
    
    
}

.top > .card{
    display: flex;
    flex-direction: row;
    column-gap: 20px;
    padding: 10px;
    
}


.container > .bottom{
        border-radius: 10px;
		box-shadow: 1px 1px 6px 2px #1DD59E;
        padding: 36px;
        
        
    }

}
    
</style>