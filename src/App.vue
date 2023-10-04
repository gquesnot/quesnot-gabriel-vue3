<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <meta charset="UTF-8">
  
  <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
  <link rel="shortcut icon" href="/src/assets/images/1-icons.svg" type="image/x-icon">
  
  
  <title>Zelda BOTW</title>
  <link rel="stylesheet" href="/src/assets/css/theme/mobirise-icons-bold.css">
  <link rel="stylesheet" href="/src/assets/css/bootstrap/bootstrap.min.css">
  <link rel="stylesheet" href="/src/assets/css/bootstrap/bootstrap-grid.min.css">
  <link rel="stylesheet" href="/src/assets/css/bootstrap/bootstrap-reboot.min.css">
  <link rel="stylesheet" href="/src/assets/css/theme/style.css">
  <link rel="preload" href="https://fonts.googleapis.com/css?family=Kiwi+Maru:300,400,500&display=swap" as="style" onload="this.onload=null;this.rel='stylesheet'">
  <noscript><link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Kiwi+Maru:300,400,500&display=swap"></noscript>
  <link rel="preload" as="style" href="/src/assets/css/theme/mbr-additional.css"><link rel="stylesheet" href="assets/css/theme/mbr-additional.css" type="text/css">
    <div style="display:flex;flex-direction:column">
    </div>
    <nav style="display:flex">
        <RouterLink  to="/">Home</RouterLink>
        <RouterLink style="margin-left:2rem" to="/monsters">Monsters</RouterLink>
      </nav>
  </header>

  <RouterView />
</template>

<style scoped>

</style>
