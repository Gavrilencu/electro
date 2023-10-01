<!-- Slider.svelte -->
<script>
  import img1 from "$lib/img/img1.jpeg";
  import img3 from "$lib/img/img3.jpeg";
  import img5 from "$lib/img/img5.jpeg";
  import { onMount, onDestroy } from "svelte";

  let currentImage = 0;
  const images = [img1, img3, img5];

  const nextImage = () => {
    currentImage = (currentImage + 1) % images.length;
  };

  const prevImage = () => {
    currentImage = (currentImage - 1 + images.length) % images.length;
  };

  let interval;

  onMount(() => {
    // Pornim automat slider-ul la fiecare 3 secunde
    interval = setInterval(() => {
      nextImage();
    }, 3000);
  });

  onDestroy(() => {
    // Oprim intervalul când componenta este distrusă
    clearInterval(interval);
  });
</script>

<div class="slider">
  <button class="btn" on:click={prevImage}>Previous</button>
  <img
    src={images[currentImage]}
    alt={`Image ${currentImage + 1}`}
    class="imgslide"
  />

  <button class="btn" on:click={nextImage}>Next</button>
</div>

<style>
  .btn {
    border: none;
    padding: 10px;
  }
  .imgslide {
    width: 50%;
    height: 100%;
    object-fit: cover;
  }
  .slider {
    display: flex;
    align-items: center;
    justify-content: space-around;
    width: 100%;
    height: 90vh;
    overflow: hidden;
  }
</style>
