<script setup>

</script>

<template>
  <div class="top">
    <div class="social-links">
      <a target="_blank" href="https://www.facebook.com/profile.php?id=100000886555648"><i
          class="bx bxl-facebook"></i></a>
      <a target="_blank" href="#"><i class="bx bxs-envelope"></i></a>
      <a target="_blank" href="https://medium.com/@chacha0519"><i class="bx bxl-medium"></i></a>
    </div>
  </div>
  <div class="separator"></div>
  <div class="bottom">
    <p>Copyright © 2024 Charlie. All Rights Reserved.</p>
  </div>
</template>

<style scoped>
.top,
.bottom {
  display: flex;
  align-items: center;
  justify-content: center;
}

.top .social-links {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 22px;
}

.separator {
  width: 100%;
  height: 1px;
  background-color: #282938;
  margin: 30px 0 20px;
}

.bottom p {
  font-size: 12px;
}

.bottom .links a {
  font-size: 12px;
  margin-left: 14px;
}

@media screen and (max-width: 768px) {
  .bottom {
    flex-direction: column-reverse;
    gap: 14px;
  }
}
</style>
