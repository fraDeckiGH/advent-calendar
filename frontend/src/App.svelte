<script>
    import Calendar from "./lib/Calendar.svelte"
    import dayjs from "dayjs"

    console.log(dayjs())
</script>

<main>
    <h1>Advent Calendar</h1>
    <hr>
    <Calendar />
</main>

<style>
    h1 {
        font-size: 2.5em;
        
        background: linear-gradient(75deg,
            hsl(209.62deg 100% 75% / 87%), 
            rgba(255, 255, 255, 0.87)
        );
        background-clip: text;
        -webkit-text-fill-color: transparent;
    }
    hr {
        margin: 2em 0 2.5em;
    }
</style>
