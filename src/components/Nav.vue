<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)
const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}
</script>

<template>
  <div class="logo" :class="{ open: menuOpen }">
    <img src="../assets/C-logo.jpg" alt="logo">
    <p>Charlie</p>
  </div>
  <ul>
    <li><a href="#main">Home</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#portfolio">Portfolio</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#feedback">Feedback</a></li>
  </ul>
  <a href="https://www.linkedin.com/in/%E4%BD%B3%E9%9C%96-%E6%9D%9C-398a64168/" target="_blank"><button>Contact Me</button></a>
  <button id="menuButton" @click="toggleMenu">
    <i class="bx bx-menu"></i>
  </button>
</template>

<style scoped>
.logo {
  display: flex;
  align-items: center;
}

.logo p {
  margin-left: 8px;
  font-weight: bold;
  font-size: 20px;
  color: #1c1e53;
}

.logo img {
  width: 40px;
  height: 40px;
}

.logo i {
  font-size: 40px;
}

ul {
  display: flex;
  gap: 40px;
}

button {
  color: #1c1e53;
  background-color: transparent;
  padding: 12px 16px;
  border-radius: 5px;
  border: 1px solid #1c1e53;
  cursor: pointer;
  transition: all 0.3s ease;
}

button:hover {
  background-color: #5e3bee;
  border-color: #5e3bee;
  color: #fff;
}

button#menuButton {
  display: none;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  padding: 7px;
}

@media screen and (max-width: 992px) {
  button {
    display: none;
  }

  ul {
    gap: 20px;
  }

  ul li a {
    font-size: 15px;
  }
}

@media screen and (max-width: 768px) {
  ul {
    display: none;
  }

  .open {
    display: none;
  }

  .open+ul {
    display: flex;
  }

  button#menuButton {
    display: flex;
  }
}

@media screen and (max-width: 576px) {
  ul li a {
    font-size: 13px;
  }

  .logo a {
    font-size: 18px;
  }
}
</style>
