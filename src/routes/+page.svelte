<script>
  import Header from "./../lib/components/Header.svelte";
import b from "$lib/img/b.jpg"
  import background from "$lib/img/img9.jpeg";
  import Slider from "../lib/components/Slider.svelte";
</script>

<Header />
<main class="app">
  <div class="dualblock">
    <div class="textblock">
      <span class="first">Lashes&Brows by Vita Lang</span>
      <span class="two">Herzlich Willkommen - im Vita Lang</span>
    </div>
    <div class="imageblock">
      <img src={b} alt="" class="imgbackground" />
    </div>
  </div>
  <Slider />
</main>

<style>
  * {
    font-family: Verdana, Geneva, Tahoma, sans-serif;
  }
  .two {
    margin-top: 50px;
    font-size: 25px;
    font-weight: 600;
  }
  .first {
    font-size: 40px;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    width: 300px;
  }
  .imgbackground {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .imageblock {
    width: 50%;
  }
  .textblock {
    width: 50%;
    display: flex;
    flex-direction: column;
  }
  .dualblock {
    margin-top: 150px;
    width: 100%;
    padding-inline: 100px;
    display: flex;
    height: 80vh;
    overflow: hidden;
  }

  .app {
    width: 100%;
    overflow: hidden;
  }
</style>
