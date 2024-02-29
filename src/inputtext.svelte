<script>
    let name = '';
    let nahom = '';
    let names = [];

    const chnage = () => {
        if (nahom !== '') {
            if (name === '') {
                name = nahom;
            } else {
                names = [...names, nahom];
            }
            nahom = '';
        }
    }
</script>

<main>
    <section class="contener">
        <div class="maincontener">
            <h6>Choose mode:</h6>
            <button class="faster">Faster responses <span>GPT 3.5 Turbo</span></button>
            <button class="better">Better responses <br> ✅ GPT 4  </button>
            <div>
                
            </div>
            {#if name === ''}
            <div>
                <h3>KAL</h3>
                <h4>Hi Nahom, What can I help you with right now, Nahom?</h4>
                
            </div>
            {:else}
            <div>
                <h2>You</h2>
                <p>{name}</p>
                
            </div>
            {#each names as n}
            <div>
                <h2>You</h2>
                <p>{n}</p>
            </div>
            {/each}
            {/if}
        </div>
    </section>
    <div class="inputfiled">
        <div class="topic">
            <h1>+</h1>
        </div>
        <input bind:value={nahom} placeholder="Ask me anything" />
        <button on:click={chnage}>→</button>
    </div>
</main>