<script>

</script>

<svelte:head>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200" />
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200" />
    <link href="https://fonts.googleapis.com/css2?family=Anton&family=Exo+2:ital,wght@0,100..900;1,100..900&family=Playwrite+BE+VLG:wght@100..400&display=swap" rel="stylesheet">
</svelte:head>


<div class="home-container">
    
    <h1>Benvenuto ed Esplora</h1>

    <p>Non sai quando poter piantare le tue piante nel tuo orto. ? </p>
    <p>Perfetto. Sei nel posto giusto !! <span class="material-symbols-outlined">mood</span></p>
    
    
</div>

<style>

@media(min-width:480px){
        .home-container{
            margin: auto;
            border-radius: 8px;
            width: 100%;
            text-align: center;

        }

        .home-container > h1{
            font-family: "Playwrite BE VLG", cursive;
            font-size: 42px;
            font-weight: 900;
        }

        .home-container > p{
            text-align: center;
            font-size: 32px;
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        }

        p > .material-symbols-outlined{
            font-size: 32px;
            color: darkgoldenrod;
            font-weight: bolder;
        }

        
    }

    
@media(max-width:480px){
        .home-container{
            margin: auto;
            border-radius: 8px;
            width: 100%;
            text-align: center;
            
        }

        .home-container > h1{
            font-family: "Playwrite BE VLG", cursive;
            font-size: 42px;
            font-weight: 900;
        }

        .home-container > p{
            text-align: center;
            font-size: 32px;
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        }

        p > .material-symbols-outlined{
            font-size: 32px;
            color: darkgoldenrod;
            font-weight: bolder;
        }
        
    }

</style>