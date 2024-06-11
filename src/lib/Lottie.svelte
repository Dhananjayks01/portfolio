<script>
  import { onMount } from 'svelte';
  import lottie from 'lottie-web';

  export let animationData; // Accept animation data as a prop

  let animationContainer;

  onMount(() => {
    const animation = lottie.loadAnimation({
      container: animationContainer,
      renderer: 'svg',
      loop: true,
      autoplay: true,
      animationData: animationData
    });

    return () => {
      animation.destroy(); // Cleanup animation on component destroy
    };
  });
</script>

<div bind:this={animationContainer} style="width: 100%; height: 100%;"></div>

<style>
  div {
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>