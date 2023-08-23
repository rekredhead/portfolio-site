<script lang="ts">
   let counter: number = 0;

   const handleClick = (e: Event) => {
      const inputElement = e.target as HTMLInputElement;
      counter = inputElement.valueAsNumber;
   }
</script>

<div class="card">
   <p>{counter}</p>
   <input on:change={handleClick} type="number" value={counter} />
</div>

<style>
   .card {
      display: flex;
      align-items: center;
      color: white;
      width: 10em;
      height: 4em;
   }
   p {
      border: 1px solid white;
      border-radius: 0.5em;
      width: 100%;
      text-align: center;
      padding: 0.5em;
      font-size: 2em;
   }
   input {
      border: none;
      outline: none;
      background-color: transparent;
      color: transparent;
      width: 1em;
      height: 100%;
   }
</style>