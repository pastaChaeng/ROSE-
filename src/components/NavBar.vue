<template>
    <nav class="rose-navbar" :class="{ 'solid-bg': isSolidBackground }">
      <div class="logo">
        <a href="/"><span><img src="../assets/rose-logo.png" class="logo-img"/></span> </a>
      </div>
      <ul class="nav-links">
        <li><a href="/">HOME</a></li>
        <li><a href="#">DISCOGRAPHY</a></li>
        <li><a href="#">GALLERY</a></li>
        <li><a href="#">ABOUT</a></li>
      </ul>
    </nav>
  </template>
  
  <script setup>
  import { ref, onMounted, onUnmounted } from 'vue';
  
  const isSolidBackground = ref(false);
  
  const handleScroll = () => {
    const scrollPosition = window.scrollY;
    if (scrollPosition > 0) {
      isSolidBackground.value = true;
    } else {
      isSolidBackground.value = false;
    }
  };
  
  onMounted(() => {
    window.addEventListener('scroll', handleScroll);
  });
  
  onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll);
  });
  </script>
  
  <style scoped>
  .rose-navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: rgba(0, 0, 0, 0); 
    padding: 1rem;
    color: white;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000; 
  }
  
  .solid-bg {
    background-color: rgba(0, 0, 0, 0.5); 
  }
  
  .logo {
    font-size: 1.5rem;
  }
  
  .nav-links {
    list-style: none;
    display: flex;
    font-size: larger;
  }
  
  .nav-links li {
    margin-right: 1rem;
  }
  
  .nav-links li a {
    color: white;
    text-decoration: none;
    padding: 0.5rem 1rem;
  }
  
  .logo-img {
    height: 3rem;
    width: 4rem;
    margin-right: 0.5rem;
  }
  </style>
  