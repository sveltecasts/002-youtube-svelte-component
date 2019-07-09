<script>
  import Youtube from "./Youtube.svelte";
  export let name;
  let video1state, video2state;
  let player1, player2;
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<button on:click={() => player1.playVideo()}>Play Video 1</button>
<button on:click={() => player2.playVideo()}>Play Video 2</button>
<br />
<Youtube
  videoId="M7lc1UVf-VE"
  on:StateChange={event => {
    video1state = event.detail;
  }}
  bind:this={player1} />
<br />
State: {video1state}
<Youtube
  videoId="lyRPyRKHO8M"
  on:StateChange={({ detail }) => (video2state = detail)}
  bind:this={player2} />
<br />
State: {video2stinitate}
