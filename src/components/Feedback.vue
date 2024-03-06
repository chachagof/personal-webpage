<script setup>
import { ref } from 'vue'

const feedbackData = ref([
  {
    id: 1,
    title: '[演算法]Floyd-Warshall',
    description: 'Floyd-Warshall algorithm，中文亦稱弗洛伊德演算法或佛洛依德演算法，是解決任意兩點間的最短路徑的一種演算法，可以正確處理有向圖或負權（但不可存在負權迴路）的最短路徑問題，同時也被用於計算有向圖的遞移閉包',
    herf: 'https://medium.com/p/668da87d91e2'
  },
  {
    id: 2,
    title: '[資料結構]Priority Queue',
    description: 'priority queue（優先佇列）是電腦科學中的一類抽象資料類型。優先佇列中的每個元素都有各自的優先級，優先級最高的元素最先得到服務，優先級相同的元素按照其在優先佇列中的順序得到服務。優先佇列通常使用「堆積」（heap）實現',
    herf: 'https://medium.com/@chacha0519/資料結構-priority-queue-28838a492a58'
  },
  {
    id: 3,
    title: '[演算法] Huffman Coding',
    description: 'Huffman Coding（霍夫曼編碼）在電腦資料處理中，使用變長編碼表對源符號（如檔案中的一個字母）進行編碼，其中變長編碼表是通過一種評估來源符號出現機率的方法得到的，出現機率高的字母使用較短的編碼，反之出現機率低的則使用較長的編碼，這便使編碼之後的字串的平均長度、期望值降低，從而達到無失真壓縮數據的目的',
    herf: 'https://medium.com/@chacha0519/演算法-huffman-coding-9c40f23d0a3b'
  }
])

const descriptionFilter = (description) => { 
  return description.length > 100 ? description.slice(0, 100).concat('...') : description
}
</script>

<template>
  <div class="title">
    <div class="left">
      <h5>My Learning Feedback</h5>
      <h3>個人心得分享</h3>
    </div>
    <a target="_blank" href="https://medium.com/@chacha0519"><button><i class="bx bxl-medium"></i>Visit My
        Medium</button></a>
  </div>
  <div class="topic">
    <div v-for="item in feedbackData" :key="item.id" class="item">
      <div class="title">
        <h5>{{ item.title }}</h5>
      </div>
      <p>
        {{ descriptionFilter(item.description) }}
      </p>
      <div class="info">
        <a target="_blank" :href="item.herf">
          <button>繼續閱讀...</button>
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.title {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

h3 {
  font-size: 48px;
  margin-top: 20px;
}

a button {
  height: 30px;
  background-color: transparent;
  padding: 20px 10px 20px 2px;
  color: #02066a;
  display: flex;
  align-items: center;
  cursor: pointer;
  border: 2px solid #02066a;
  border-radius: 10px;
  font-size: 15px;
}

a button:hover {
  background-color: #02066a;
  color: #fff;
}

.topic {
  margin-top: 50px;
  display: flex;
  gap: 40px;
}

.topic .item {
  display: flex;
  flex-direction: column;
  gap: 20px;
  border: 2px solid #006b6a;
  border-radius: 10px;
  padding: 30px;
  transition: all 0.3s ease;
}

.topic .item .title {
  color: #006b6a;
  font-size: 22px;
}

.topic .item:hover {
  border-color: #5e3bee;
}

.topic .item p {
  line-height: 22px;
  font-size: 14px;
}

.topic .item .info {
  display: flex;
  justify-content: end;
}

.topic .item .info a button {
  margin-top: 40px;
  cursor: pointer;
  background-color: #fff;
  color: #006b6a;
  padding: 5px;
  border: 1px solid #006b6a;
  border-radius: 5px;
  transition: all 0.3s ease;
}

.topic .item .info a button:hover {
  background-color: #006b6a;
  color: #fff;
}

@media screen and (max-width: 1200px) {
  h3 {
    font-size: 32px;
  }

  .topic .item .title {
    font-size: 20px;
  }

  .topic .item p {
    font-size: 13px;
  }
}

@media screen and (max-width: 992px) {
  .topic {
    gap: 14px;
    flex-wrap: wrap;
    justify-content: center;
  }

  .topic .item {
    width: 48%;
  }
}

@media screen and (max-width: 576px) {
  .topic .item {
    width: 100%;
  }
}
</style>
