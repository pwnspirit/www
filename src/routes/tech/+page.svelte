<script>
    let cards = [
        [
            "Earlymoon",
            "https://github.com/pwnspirit/earlymoon",
            " 🌙 DNS query tool written in go ",
            "--red",
        ],
        [
            "GOcrt",
            "https://github.com/pwnspirit/gocrt",
            "a cat that follows your cursor around",
            "--peach",
        ],
        [
            "CTF Writeups",
            "https://github.com/pwnspirit/pwnotes",
            "My ctf writeups and some of notes",
            "--green",
        ],
    ];
</script>

<svelte:head>
    <meta property="og:description" content="tech stuff" />
    <meta name="theme-color" content="#94e2d5" />
    <title>pwnspirit/tech</title>
</svelte:head>

<div class="contents">
    <p class="tech-text">
        This page is more appropriately titled "tech", but that doesn't fit in 4 characters.<br />
        <a href="https://github.com/pwnspirit/nix" target="_blank" class="link">dotfiles</a>,
        
    </p>
    <div class="cards">
        {#each cards as [title, link, desc, color]}
            <a
                href={link}
                target="_blank"
                rel="noreferrer"
                class="card"
                style=" --card-color: var({color});"
            >
                <h1 class="card-title">
                    {title}
                </h1>
                <span class="card-body">
                    {desc}
                </span>
            </a>
        {/each}
    </div>
    <div id="Kit">
    </div>
</div>

<style>

    .link {
        color: var(--blue);
    }
    .link:hover {
        text-shadow: 0 0 5px;
    }

    .cards {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
        gap: 50px;
        max-width: 1200px;
    }

    div > .card {
        text-decoration: none;
        background-color: var(--mantle);
        color: var(--text);
        border: 1px solid;
        border-radius: 10px;
        max-width: 270px;
        min-height: 120px;
        text-align: left;
        padding: 20px;
        display: flex;
        flex-direction: column;
        border-color: var(--card-color); 
        color: var(--card-color);
        transition: background linear 0.25s;
    }

    .card:hover {
        background-color: var(--card-color);
        color: var(--crust);
    }

    .card:hover > .card-body {
        color: var(--crust);
    }

    .card-title {
        font-size: 30px;
        margin: 0;
        padding: 0;
        color: var(--card-color);
        margin-bottom: 10px;
    }

    .card-body {
        padding: 0 0 5px;
        margin: 0;
    }

    .card:hover > .card-title {
        color: var(--crust);
    }

    .tech-text {
        text-align: center;
        max-width: 800px;
        margin-bottom: 0;
    }

    .contents {
        justify-content: flex-start;
        gap: 50px;
    }


</style>
