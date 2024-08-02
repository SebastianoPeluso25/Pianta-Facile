<script>
	import { scale } from 'svelte/transition';
	import { expoInOut } from 'svelte/easing';

export let title;
	export let description;
    export let img;
    export let link;
	export let tag;


</script>



<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Exo+2:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Anton&family=Exo+2:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">
</svelte:head>



<a href={link} > 
<section class="card"
		transition:scale={{duration: 1000, easing: expoInOut}}>
		
		<div class="item" >
            <img src={img} alt="">
            <p>{title}</p>
			
		</div>

</section>
</a>


<style>

@media(min-width:480px){
		.card { 
	
			width: 200px;
			box-shadow: 1px 1px 6px 2px #1DD59E;
			margin: 8px auto;
			background-color: white;	
		}

		.card:hover{
			box-shadow: 10px 10px 0px #73DAB9;
			top: -5px;
			left: -5px;
			border-radius: 4px;
			transition: ease-in-out;
			
			
		}

		a{
			text-decoration: none;
			color: green;
		}

		a:hover{
			color: black;
			transition-duration: 1s;
		}

		.item {
			display: flex;
			flex-direction: column;
			align-items: center;
			text-align: center;
			font-size: 25px;
			width: 100%;
			background-color: #BFFFC7;
			
			
			
		}


        .item > p{
			
            
			font-family: "Anton", sans-serif;
        }
        .item > img{
            width: 100%;
            height: 120px;
        }



	}

	/**MOBILE  */

	@media(max-width:480px){
		.card { 
	
	width: 200px;
	box-shadow: 1px 1px 6px 2px #1DD59E;
	margin: 8px auto;
	background-color: white;	
}

.card:hover{
	box-shadow: 10px 10px 0px #73DAB9;
	top: -5px;
	left: -5px;
	border-radius: 4px;
	transition: ease-in-out;
	
	
}

a{
	text-decoration: none;
	color: green;
}

a:hover{
	color: black;
	transition-duration: 1s;
}

.item {
	display: flex;
	flex-direction: column;
	align-items: center;
	text-align: center;
	font-size: 25px;
	width: 100%;
	background-color: #BFFFC7;
	
	
	
}


.item > p{
	
	
	font-family: "Anton", sans-serif;
}
.item > img{
	width: 100%;
	height: 120px;
}

	
	}

</style>