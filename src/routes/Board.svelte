<script>
    let selectedX, selectedY;
    let lista = [1,2,3,4,5];
</script>

<select bind:value={selectedX}>
    {#each lista as item}
         <option value="{item}">{item}</option>
    {/each}
</select>

<p>Wybrałeś: {selectedX}</p>

<div class="grid grid-cols-{selectedX} gap-4 justify-items-center">
    {#each Array(selectedX) as x}
        {#each Array(selectedX) as x}
            <img src="./assets/svelte.png" class="w-max" />
        {/each}
    {/each}
</div>
