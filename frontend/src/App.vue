<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <img
          alt="Pallets logo"
          class="logo"
          src="@/assets/logo.jpg"
          width="125"
          height="125"
        />
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/form">Form</RouterLink>
        <RouterLink to="/formdisplay">Form Display</RouterLink>
        <RouterLink to="/aboutus">About Us</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
</style>
