<script setup>
import avatarImage from '../assets/Avatar.jpg'
import armyImage from '../assets/army.png'
</script>

<template>
  <div class="left">
    <img :src="avatarImage" alt="about" />
  </div>
  <div class="right">
    <h5>Experience</h5>
    <h3>工作經驗</h3>
    <div class="title">
      <div class="title-logo">
        <img :src="armyImage" alt="army" />
      </div>
      <div class="work">
        <h4>航空電子修護士 • 中華民國國軍</h4>
        <span>二月 2018 - 六月 2022</span>
      </div>
    </div>
    <ul>
      <li>
        1.每日執行直升機及航空裝備保養暨檢查，在就任期間無因個人因素肇生任何飛安意外
      </li>
      <li>
        2.多次參與各項國軍重大演習並且帶領20人以上部隊完成上級交付任務
      </li>
      <li>
        3.在符合相關規定及各項安全下，透過自身規劃任務方向，減少30%人力及時間成本，完成相同任務，屢獲讚賞
      </li>
    </ul>
  </div>
</template>

<style scoped>
.left {
  border-radius: 10px 10px 0 0;
}

.left img {
  width: 440px;
  border-radius: 15px;
}

.right h3 {
  font-size: 48px;
  margin-top: 20px;
}

.right .title {
  display: flex;
  align-items: center;
  margin-top: 10px;
}

.right .title .title-logo {
  width: 100px;
  height: 100%;
  margin-right: 10px;
}

.right ul li {
  font-size: 16px;
  margin-top: 15px;
}

@media screen and (max-width: 1200px) {
  .left img {
    width: 370px;
  }

  .right h3 {
    font-size: 32px;
  }
}
</style>
