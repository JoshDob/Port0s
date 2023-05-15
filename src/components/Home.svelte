<script>
  import { onMount } from 'svelte';
  let color = "white";

  function changeColor() {
    color = color === "white" ? "black" : "white";
  }

  onMount(() => {
    setInterval(changeColor, 2000); // changes color every 2 seconds
  });
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@700&display=swap');

  .animated-text {
    font-family: 'Roboto Mono', monospace;
    font-size: 3em;
    text-align: center;
    margin-top: 30%;
    animation: fadeIn 3s ease-in-out;
  }

  @keyframes fadeIn {
    from {opacity: 0;}
    to {opacity: 1;}
  }
</style>

<div class="animated-text" style="background-color: {color}; transition: background-color 0.5s ease;">
  Welcome to My Portfolio
</div>
