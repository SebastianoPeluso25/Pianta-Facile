<script>

    import Calendar from "../../lib/components/calendar.svelte";

    let events = {
        '2024-07-15': 'event-red',
        '2024-07-16': 'event-red',
        '2024-07-17': 'event-red',
        '2024-07-18': 'event-red',
        '2024-07-19': 'event-red',
        '2024-07-20': 'event-red',
        '2024-07-21': 'event-red',
        '2024-07-22': 'event-red',
        '2024-07-23': 'event-red',
        '2024-07-24': 'event-red',
        '2024-07-25': 'event-red',
        '2024-07-26': 'event-red',
        '2024-07-27': 'event-red',
        '2024-07-28': 'event-red',
        '2024-07-29': 'event-red',
        '2024-07-30': 'event-red',
        '2024-07-31': 'event-red',
    };

    let events2 = {
        '2024-07-15': 'event-red',
        '2024-07-16': 'event-red',
        '2024-07-17': 'event-red',
        '2024-07-18': 'event-red',
        '2024-07-19': 'event-red',
        '2024-07-20': 'event-red',
        '2024-07-21': 'event-red',
        '2024-07-22': 'event-red',
        '2024-07-23': 'event-red',
        '2024-07-24': 'event-red',
        '2024-07-25': 'event-red',
        '2024-07-26': 'event-red',
        '2024-07-27': 'event-red',
        '2024-07-28': 'event-red',
        '2024-07-29': 'event-red',
        '2024-07-30': 'event-red',
        '2024-07-31': 'event-red',
    };



</script>

<svelte:head>
  <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Dancing+Script&family=Edu+AU+VIC+WA+NT+Hand:wght@400..700&family=Pacifico&family=Poetsen+One&display=swap" rel="stylesheet">
</svelte:head>


<h1>Zucchine</h1>

<div class="table">
    <div class="row semina">
      <h2>Semina</h2>
      <div class="months semina">
        <div class="circle one">Aprile</div>
        <div class="circle two">Maggio</div>
      </div>
    </div>
    <div class="row trapianto">
      <h2>Trapianto</h2>
        <div class="months trapianto">
            <div class="circle one">Maggio</div>
            <div class="circle two">Giugno</div>
        </div>
      </div>
  </div>



<style>

@media(min-width:480px){

.table{
  margin: auto;
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-items: center;
  align-items: center;
  align-content: center;
  justify-content: space-evenly;
  
}

.table > .row{
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 10px;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  border-radius: 8%;
  
  
}

.table > .semina{
  border-bottom: 4px solid #2bb6bb;
  
}

.table > .trapianto{
  border-bottom: 4px solid #2bb6bb;
  
}

.row > .months{
  display: flex;
  flex-direction: row;
  column-gap: 10px;
  
  width: 100%;
}
.months > .circle{
  text-transform: uppercase;
  color: white;
  border-radius: 50%;
  padding: 10px;
  font-family: "Anton", sans-serif;
  font-size: 18px;
  
}


.semina > .one{
  background-color: #c7be41;
}
.semina > .two{
  background-color: #e7ad2e;
}
.trapianto > .one{
  background-color: #c7be41;
}
.trapianto > .one{
  background-color: #e7ad2e;
}
.trapianto > .two{
  background-color: #f37610;
}



.calendari{
    
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr;
    text-align: center;
    justify-content: center;
    padding: 20px;

    
}

h1{
  font-family: "Poetsen One", sans-serif;
  font-size: 40px;
  text-align: center;
}
}


@media(max-width:480px){

.table{
  margin: auto;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-items: center;
  align-items: center;
  align-content: center;
  justify-content: space-evenly;
  
}

.table > .row{
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 10px;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  border-radius: 8%;
  
  
}

.table > .semina{
  border-bottom: 4px solid #2bb6bb;
  
}

.table > .trapianto{
  border-bottom: 4px solid #2bb6bb;
  
}

.row > .months{
  display: flex;
  flex-direction: row;
  column-gap: 10px;
  
  width: 100%;
}
.months > .circle{
  text-transform: uppercase;
  color: white;
  border-radius: 50%;
  padding: 10px;
  font-family: "Anton", sans-serif;
  font-size: 18px;
  
}

.semina > .one{
  background-color: #2bb6bb;
}
.semina > .two{
  background-color: #c7be41;
}
.semina > .three{
  background-color: #e7ad2e;
}
.trapianto > .one{
  background-color: #c7be41;
}
.trapianto > .two{
  background-color: #e7ad2e;
}
.trapianto > .three{
  background-color: #f37610;
}



.calendari{
    
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr;
    text-align: center;
    justify-content: center;
    padding: 20px;

    
}

h1{
  font-family: "Poetsen One", sans-serif;
  font-size: 40px;
  text-align: center;
}
}

    

</style>