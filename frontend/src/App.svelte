<script>
    import svelte_logo from "./assets/svelte.svg"
    import Counter from "./lib/Counter.svelte"

    import dayjs from "dayjs"

    console.log(dayjs())
</script>

<main>
    <a
        href="https://svelte.dev/docs/svelte/overview"
        target="_blank"
        rel="noreferrer"
    >
        <img src={svelte_logo} class="logo svelte" alt="Svelte Logo" />
    </a>
    <h1>Template frontend with Svelte</h1>

    <div class="card">
        <Counter />
    </div>

    <p class="read-the-docs">Click on the Svelte logo to learn more</p>
</main>

<style>
    .logo {
        margin: 0 auto;
        height: 6em;
        padding: 1.5em;
        will-change: filter;
        transition: filter 300ms;

        &:hover {
            filter: drop-shadow(0 0 2em #ff3e00aa);
        }
    }
    .read-the-docs {
        color: #afafaf;
    }
</style>
