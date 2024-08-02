<script>
    import { onMount } from "svelte";
  
    export let selectedDate;

  
    let currentDate = new Date();
    let currentMonth = currentDate.getMonth();
    let currentYear = currentDate.getFullYear();
    let daysInMonth = new Date(currentYear, currentMonth + 1, 0).getDate();
    let firstDay = new Date(currentYear, currentMonth, 1).getDay();
    export let events = {};
  
    function getDayClass(day) {
      let date = `${currentYear}-${String(currentMonth + 1).padStart(2, '0')}-${String(day).padStart(2, '0')}`;
      return events[date] || '';
    }
  
    function handleDayClick(day) {
      let date = `${currentYear}-${String(currentMonth + 1).padStart(2, '0')}-${String(day).padStart(2, '0')}`;
      onDateSelect(date);
    }
  </script>
  

  
  <div class="calendar">
    {#each Array(firstDay).fill(0) as _}
      <div class="day"></div>
    {/each}
    {#each Array(daysInMonth).fill(0).map((_, i) => i + 1) as day}
      <div
        class="day {getDayClass(day)} {selectedDate === `${currentYear}-${String(currentMonth + 1).padStart(2, '0')}-${String(day).padStart(2, '0')}` ? 'selected' : ''}"
        on:click={() => handleDayClick(day)}
      >
        {day}
      </div>
    {/each}
  </div>


  <style>
    .calendar {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      gap: 10px;
      
      max-width: 400px;
      margin: 20px auto;
      padding: 20px;
      background-color: #f9f9f9;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      margin: auto;
      
    }
    .day {
      width: 50px;
      height: 50px;
      display: flex;
      justify-content: center;
      align-items: center;
      
      font-weight: bold;
      color: #333;
      background-color: #fff;
      border-radius: 50%;
      cursor: pointer;
      transition: transform 0.2s;
    }
    .day:hover {
      transform: scale(1.1);
    }
    .event-red {
      background-color: #ff6b6b;
      color: #fff;
    }
    .event-blue {
      background-color: #4dabf7;
      color: #fff;
    }
    .event-green {
      background-color: #51cf66;
      color: #fff;
    }
    .selected {
      border: 2px solid #000;
    }
  </style>
  