<script setup>

</script>

<template>
  <h5>My Skills</h5>
  <h3>專長</h3>
  <div class="skill-items">
    <div class="item">
      <div class="icon"><i class="bx bxs-chalkboard"></i></div>
      <h4>Front-end</h4>
      <ul>
        <li>HTML <i class="bx bxl-html5"></i></li>
        <li>CSS <i class="bx bxl-css3"></i></li>
        <li>Javascript(ES6+) <i class="bx bxl-javascript"></i></li>
        <li>VUE3 <i class="bx bxl-vuejs"></i></li>
        <li>Bootstrap <i class="bx bxl-bootstrap"></i></li>
      </ul>
    </div>
    <div class="item">
      <div class="icon"><i class="bx bxs-data"></i></div>
      <h4>Back-end</h4>
      <ul>
        <li>Node.js <i class="bx bxl-nodejs"></i></li>
        <li>Express <i class="bx bx-check-circle"></i></li>
        <li>MySQL <i class="bx bx-check-circle"></i></li>
        <li>MongoDB <i class="bx bxl-mongodb"></i></li>
      </ul>
    </div>
    <div class="item">
      <div class="icon"><i class="bx bxl-figma"></i></div>
      <h4>Other</h4>
      <ul>
        <li>Git/Github <i class="bx bxl-github"></i></li>
        <li>Git Flow/Github Flow <i class="bx bx-check-circle"></i></li>
        <li>Heroku <i class="bx bxl-heroku"></i></li>
        <li>Postman <i class="bx bx-check-circle"></i></li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
h3 {
  font-size: 48px;
  margin-top: 20px;
}

.skill-items {
  display: flex;
  margin-top: 70px;
  gap: 30px;
}

.skill-items .item {
  background-color: #deebee;
  width: 25%;
  border-radius: 10px;
  padding: 32px;
  border-bottom: 4px solid transparent;
  cursor: pointer;
  transition: all 0.3s ease;
}

.skill-items .item:hover {
  border-color: #5e3bee;
}

.skill-items .item .icon {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #fff;
  width: 46px;
  height: 46px;
  border-radius: 10px;
  margin-bottom: 22px;
  box-shadow: 0 0 16px rgba(0, 0, 0, 0.1);
}

.skill-items .item .icon i {
  font-size: 26px;
  color: #006b6a;
}

.skill-items .item h4 {
  font-size: 18px;
}

skill-items .item ul li {
  display: flex;
  align-items: center;
  margin-top: 20px;
  font-size: 14px;
  line-height: 3px;
  color: #1c1e53;
}

.skill-items .item ul li i {
  font-size: 20px;
}

@media screen and (max-width: 1200px) {
  .skill-items {
    gap: 10px;
    justify-content: space-between;
    flex-wrap: wrap;
  }

  .skill-items .item {
    width: 49%;
  }
}

@media screen and (max-width: 768px) {
  .skill-items {
    gap: 8px;
  }
}

@media screen and (max-width: 576px) {
  .skill-items .item {
    width: 100%;
  }
}
</style>
