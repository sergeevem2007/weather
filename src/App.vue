<script setup lang="ts">
import Weather from './components/Weather.vue'
</script>

<template>
  <header>
    <div class="container">
      <div class="header__wrapper">
        <a href="/" class="header__logo">
          <img width="48" height="48" src="https://img.icons8.com/fluency/48/smiling-sun.png" alt="smiling-sun"/>
          <span>weather forecast</span>
        </a>
      </div>
    </div>
  </header>

  <main>
    <Weather/>
  </main>
</template>

<style scoped>
  .header__wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 24px 0;
  }
  .header__logo {
    display: flex;
    align-items: center;
    font-weight: 900;
    font-size: 32px;
    text-decoration: none;
    text-transform: uppercase;
    line-height: 1;
    color: var(--color-link);
  }
</style>
