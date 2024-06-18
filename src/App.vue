<script setup>
import NavBar from './components/NavBar.vue';
import BlackPinkRose from './components/BlackPinkRose.vue'
</script>

<template>
  <div id="app">
    <header>
      <NavBar />
    </header>

    <main>
      <video autoplay muted loop class="video-background" src="./assets/roseanne-vid.mp4"></video>
      <section class="content">
        <div class="browse-link">
          <a href="/">CONTINUE TO WEBSITE </a>
        </div>
      </section>
    </main>
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html, body, #app {
  height: 100%;
  width: 100%;
  overflow-x: hidden;
  font-family: 'Roboto', sans-serif;
  background-color: #0d1117; /* GitHub dark theme background */
  color: #c9d1d9; /* GitHub dark theme text color */
}

header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1;
  background-color: #161b22; /* Slightly darker background for header */
  padding: 10px 0;
}

.video-background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: 0;
}

main {
  position: relative;
  z-index: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  text-align: center;
}

.content {
  position: relative;
  z-index: 1;
  text-align: center;
  justify-items: center;
  display: flex;
  padding: 10px;
  border-radius: 10px;
}

.browse-link a {
  color: white; /* GitHub link color */
  text-decoration: none;
  font-size: 1.5em;
  transition: color 0.3s;
  font-size:xx-large;
  font-family:'Courier New', Courier, monospace;
  bottom: 60px;
  right: 34%;
  font-weight: 100;
}

.browse-link a:hover {
  color: #6f819c; /* Darker shade on hover */
}
</style>
