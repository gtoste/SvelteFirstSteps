<script>
    async function getRandomNumber() {
		const res = await fetch(`https://private-anon-f14eb8cf60-carsapi1.apiary-mock.com/manufacturers`);
		const text = await res.json();
        

		if (res.ok) {
			return text;
		} else {
			throw new Error(text);
		}
	}

	let promise = getRandomNumber();
</script>
{#await promise}
    ..waiting
{:then data} 
    <div class="grid grid-cols-2 bg-gray-700 gap-1">
        {#each data as cars}
        <div class="bg-gray-200">
            <h1>{cars.name}</h1>
            <h3>{cars.avg_price}$</h3>
            <h3>{cars.avg_horsepower}</h3>
        </div>
        {/each}
        
    </div>
{/await}