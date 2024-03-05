<script setup>
import { ref } from 'vue'
import shoppingSiteImage from '../assets/shopping-site.png'
import simpleTweeterImage from '../assets/simple-tweeter.png'
import snakeGameImage from '../assets/snake-game.jpg'

const portfolio = ref([
  {
    id: 1,
    img: shoppingSiteImage,
    title: '線上購物網站',
    description: '擁有會員系統的線上購物網站，使用者依照需求分為訪客、買家、賣家，不同類型的訪客享受不同的網站功能。買家擁有個人獨立購物車，賣家擁有個人獨立商店頁面，訪客僅能瀏覽商品。由個人獨立開發，開發規格以前後分離的方式進行。前端使用 VUE3 打造，後端使用 Node.js 加上 MySQL 資料庫作共同開發。',
    herf: 'https://chachagof.github.io/shopping-site-front-end/',
    showContent: false
  },
  {
    id: 2,
    img: simpleTweeterImage,
    title: 'Simple Twitter',
    description: '由 3人團隊運用Node.js、Express 和 MySQL， 以全端模式開發的社群網站。供使用者推文、按讚、追蹤他 人，並可在公開聊天室聊天，另設有後台供管理員瀏覽使用者數據、管理 文章。',
    herf: '#',
    showContent: false
  },
  {
    id: 3,
    img: snakeGameImage,
    title: 'Snake game',
    description: '使用 VUE3 為框架，透過簡單的程式碼完成懷舊小遊戲，使用 RWD 讓使用者在螢幕較小時可以使用鍵盤遊玩，並使用 Localstorge 來紀錄最高分，使遊戲更有挑戰性',
    herf: 'https://chachagof.github.io/snake-game/',
    showContent: false
  }
])

const contentShow = (content, show) => {
  return show ? content : content.slice(0, 70).concat('......')
}

const showFullContent = (index) => {
  portfolio.value[index].showContent = !portfolio.value[index].showContent
}

</script>

<template>
  <div class="header">
    <div class="info">
      <h5>My Portfolio</h5>
      <h3>作品集</h3>
    </div>
  </div>

  <div class="portfo-items">
    <div v-for="(item, index) in portfolio" :key="item.id" class="item">
      <img :src="item.img" />
      <div class="info">
        <h4>{{ item.title }}</h4>
        <p> {{ contentShow(item.description, item.showContent) }} </p>
        <button @click="showFullContent(index)">繼續閱讀</button>
        <a :href="item.herf">前往網站<i class="bx bx-link-external"></i></a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 60px;
}

.portfolio .header h3 {
  font-size: 48px;
  margin-top: 20px;
}

.header button i {
  font-size: 26px;
}

.portfo-items {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.portfo-items .item {
  width: 30%;
  background-color: #fff;
  border-radius: 10px;
  border-bottom: 4px solid transparent;
  cursor: pointer;
  box-shadow: 0 5px 32px rgba(0, 0, 0, 0.15);
  transition: all 0.3s ease;
}

.portfo-items .item:hover {
  border-color: #5e3bee;
}

.portfo-items .item img {
  width: 100%;
  height: 240px;
  object-fit: cover;
  object-position: top;
  border-radius: 10px 10px 20px 20px;
}

.portfo-items .item .info {
  display: flex;
  flex-direction: column;
  gap: 14px;
  padding: 20px 32px 42px;
}

.portfo-items .item .info h4 {
  font-size: 18px;
}

.portfo-items .item .info p {
  font-size: 13px;
}

.portfo-items .item .info button {
  background-color: transparent;
  border: none;
  cursor: pointer;
  color: #777676;
  text-align: end;
}

.portfo-items .item .info a {
  text-decoration: underline;
  text-underline-offset: 10px;
  text-decoration-color: #5e3bee;
}

.portfo-items .item .info a i {
  margin-left: 2px;
  font-size: 16px;
}

@media screen and (max-width: 1200px) {
  .header h3 {
    font-size: 32px;
  }
}

@media screen and (max-width: 992px) {
  .portfo-items {
    gap: 22px;
    flex-wrap: wrap;
    justify-content: center;
  }

  .portfo-items .item {
    width: 48%;
  }
}

@media screen and (max-width: 768px) {
  .portfo-items {
    gap: 18px;
  }
}

@media screen and (max-width: 576px) {
  .header button {
    font-size: 12px;
    padding: 8px 14px;
  }

  .portfo-items .item {
    width: 80%;
  }
}
</style>
