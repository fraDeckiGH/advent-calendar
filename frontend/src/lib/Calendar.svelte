<script lang="ts">
    import Day from "./Day.svelte"
</script>


<div class="calendar">
    {#each Array(24) as _, index}
        <Day numberWithinMonth={index + 1} />
    {/each}
</div>


<style>
    .calendar {
        display: grid;
        grid-template-columns: repeat(6, 1fr);
        gap: 1em;
        grid-auto-rows: minmax(11em, auto);
    }
</style>
