<template>
  <div class="left">
    <h3>嗨，我是杜佳霖 Charlie</h3>
    <h5>這是我的<span>個人介紹</span>網站</h5>
    <p>
      我透過網路課程 ALPHAcamp
      學習程式語言，藉由課程的漸進式學習，以及自己對於程式語言的喜愛，在這期間掌握了網頁前後端相關的基礎技術及一些熱門框架如<b>VUE3</b>、<b>Node.js</b>等，也因為對於學習的熱愛，在既有課程之外也有持續在學習相關知識，並透過<b>
        Medium 分享自身學習後的心得</b>，也希望透過我熱情與實力，成為一名合格的全端工程師。
    </p>
    <a target="_blank" href="https://www.cakeresume.com/me/du-chacha">
      <button>Get In Touch</button>
    </a>
  </div>
  <div class="right">
    <img src="../assets/Avatar.jpg" alt="杜佳霖大頭貼 My Avatar" />
  </div>
</template>

<style scoped>
.left {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.left h3 {
  margin-bottom: 10px;
  font-weight: bold;
  font-size: 46px;
}

.left h5 span {
  color: #5e3bee;
}

.left p {
  color: #1c1e53;
  font-size: 22px;
  margin-top: 30px;
  line-height: 30px;
}

.left button {
  margin-top: 40px;
  color: #fff;
  cursor: pointer;
  background-color: #5e3bee;
  padding: 14px 14px;
  border: 1px solid transparent;
  border-radius: 5px;
}

.right img {
  width: 500px;
  border-radius: 20px;
}

@media screen and (max-width: 1200px) {
  .left h5 {
    font-size: 18px;
  }

  .left h3 {
    font-size: 36px;
  }

  .left p {
    font-size: 18px;
  }

  .right img {
    width: 380px;
  }
}

@media screen and (max-width: 576px) {
  .left h3 {
    font-size: 32px;
  }

  .left p {
    font-size: 16px;
  }

  .left button {
    width: 100%;
  }
}
</style>
