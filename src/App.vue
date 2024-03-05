<script setup>
import Nav from './components/Nav.vue'
</script>

<template>
  <nav>
    <Nav />
  </nav>
</template>

<style scoped>
nav {
  background-color: #fff;
  position: sticky;
  top: 0;
  padding: 0 85px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 80px;
  box-shadow: 0 5px 80px rgba(0, 0, 0, 0.1);
}

@media screen and (max-width: 768px) {
  nav {
    justify-content: space-between;
    padding: 0 42px;
  }
}
</style>
