<script>
  import Inpu from "./inputtext.svelte";

  let Visible = false;
  let accountVisible = true;

  function Visibility() {
    accountVisible = false;

    setTimeout(() => {
      Visible = true;
    }, 2000);
  }
</script>

<main>
  <img src="/img/logo.png" alt="loggo" class="logo">
  {#if Visible}
    <button class="topics">◷</button>
    <button class="upgrade">Upgrade to Pro</button>
    <button class="logged">logged in as</button>
    <a href="as" class="feed"><p>Send Feedback 💡</a>
    <p class="words"><b>14,842 </b>words left</p>
    <Inpu/>
  {/if}

  {#if accountVisible}
    <div class="account">
      <div class="center">
        <h2>Continue with</h2>
        <button on:click={Visibility} class="google">Google</button>
        <button on:click={Visibility} class="gitHub">GitHub</button>
        <p>Need help? Contact <a href="as">support@kal.chat</a></p>
      </div>
    </div>
  {/if}
</main>

<style>
  .account {
    display: grid;
    place-items: center;
    margin-top: 310px;
  }
  
</style>