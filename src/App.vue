<script setup>
import Nav from './components/Nav.vue'
import Introduction from './components/Introduction.vue'
import Skill from "./components/Skill.vue"
import Portfolio from './components/Portfolio.vue'
import Experience from './components/Experience.vue'

</script>

<template>
  <nav>
    <Nav />
  </nav>
  <main>
    <Introduction />
  </main>
  <div class="skills" id="skills">
    <Skill />
  </div>
  <div class="portfolio" id="portfolio">
    <Portfolio />
  </div>
  <div class="experience" id="experience">
    <Experience />
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

.portfolio {
  padding: 110px 85px;
}

.experience {
  background-color: #deebee;
  padding: 110px;
  display: flex;
  align-items: center;
  gap: 60px;
}

@media screen and (max-width: 992px) {
  main {
    flex-direction: column;
  }

  .experience {
    flex-direction: column;
    justify-content: center;
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

  .portfolio {
    padding: 60px 42px;
  }

  .experience {
    padding: 85px 42px;
  }
}
</style>
