<script>

</script>

<svelte:head>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
</svelte:head>

<footer>
    <div class="contact">
        <p>FOOTER SPACE</p>
        
    </div>
</footer>


<style>

:global(body){
    padding: 0;
    margin: 0;
}

    @media(max-width:480px){

    }

    @media(min-width:480px){
        footer{
            background-color: #73a942;
            
            border-top: 10px solid #245501;
            text-align: center;
            color: white;
            font-size: 20px;
            width: 100%;
            height: 100px;
        }

        footer > .contact{
            display: flex;
            margin: auto;
            flex-direction: column;
            

        }
    }

    @media(max-width:480px){
        footer{
            background-color: #73a942;
            
            border-top: 10px solid #245501;
            text-align: center;
            color: white;
            font-size: 20px;
            width: 100%;
            
        }

        footer > .contact{
            display: flex;
            margin: auto;
            flex-direction: column;
            

        }
    }



</style>