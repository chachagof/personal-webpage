<script setup>
import Nav from './components/Nav.vue'
import Introduction from './components/Introduction.vue'
import Skill from "./components/Skill.vue"

</script>

<template>
  <nav>
    <Nav />
  </nav>
  <main>
    <Introduction />
  </main>
  <div class="skills">
    <Skill />
  </div>
</template>

<style>
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

main {
  background-color: #deebee;
  padding: 90px 85px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 40px;
}

.skills {
  padding: 110px 85px 0;
}

@media screen and (max-width: 992px) {
  main {
    flex-direction: column;
  }
}

@media screen and (max-width: 768px) {
  nav {
    justify-content: space-between;
    padding: 0 42px;
  }

  main {
    padding: 42px;
  }

  .skills {
    padding: 85px 42px 0;
  }
}
</style>
