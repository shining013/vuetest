<template>
  <div class="container secWrap">
    <h3>HOT & NEW</h3>
    <div class="cardWrap">
      <div class="card" v-for="(item, i) in data_m" v-bind:key="i">
        <div class="imgWrap">
          <img v-bind:src="`./images/${item.img}`" alt="" />
        </div>
        <div class="cardText">
          <h1>{{ item.title }}</h1>
          <p>🍿 {{ item.num }}</p>
          <p>대여 :{{ item.won }}</p>
        </div>
      </div>
    </div>
  </div>

  <!-- <div v-for="(item, index) in todos" v-bind:key="index">{{ item }}</div>

    <ul>
      <li v-for="(item, i) in todos" :key="i">{{ item }}</li>
    </ul> -->
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      data_m: [
        { title: "탈주", num: "8.1", won: "11,000", img: "Escape.jpg" },
        {
          title: "악은 존재하지 않는다",
          num: "8.0",
          won: "10,890",
          img: "evil.jpg",
        },
        { title: "파묘", num: "7.8", won: "9,900", img: "dead.jpg" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "./assets/css/style.scss";
.secWrap {
  padding: 5px 16px;
  background-color: #fff;
}
.cardWrap {
  display: flex;
  gap: 10px;
  .card {
    width: 212px;
    img {
      width: 100%;
    }
    .imgWrap {
      width: 100%;
      overflow: hidden;
      border-radius: 10px;
      img {
        display: block;
        width: 100%;
        transition: 0.3s;
      }
      &:hover img {
        transform: scale(1.05);
      }
    }
    .cardText {
      padding: 5px;
      font-size: 12px;
    }
  }
}
</style>
