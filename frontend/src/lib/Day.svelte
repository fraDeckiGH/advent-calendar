<script lang="ts">
    import { fade } from 'svelte/transition';
    
    let { numberWithinMonth }: { numberWithinMonth: number } = $props()
    
    const img_size = { width: 100, height: 86 }
    let img_url = $derived(`https://placehold.co/${img_size.width}x${img_size.height}?text=Day+${numberWithinMonth}`)
    
    let msg = $derived(`Day ${numberWithinMonth} - Surprise!`)
    let revealed = $state(false)
    
    function reveal() {
        revealed = true
    }
</script>


<button class="card day" onclick={reveal}>
    {#if revealed}
        <div transition:fade={{ duration: 200 }}>
            <img {...img_size}
                src={img_url}
                alt="Placeholder"
            />
            <p class="msg">{msg}</p>
        </div>
    {:else}
        <span class="num-lbl">
            Day {numberWithinMonth}
        </span>
    {/if}
</button>


<style>
    .day {
        background-image: linear-gradient(to right, hsl(239 32% 17% / 100%), transparent);
        box-shadow: 0 .5rem 1rem rgba(0, 0, 0, .15);
    }
    
    img {
        border-radius: var(--border-radius);
    }
    .msg {
        margin-top: .75em;
    }
    
    .num-lbl {
        font-size: 1.1em;
    }
</style>
