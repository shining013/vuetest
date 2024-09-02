<template>
  <div class="container secWrap">
    <img src="./assets/images/Escape.jpg" alt="" />
    <div class="card">
      <h1>{{ title }}</h1>
      <p>🍿 {{ num }}</p>
      <p>대여 :{{ won }}</p>
    </div>
    
    {{ todos[0] }}
    <div v-for="(item, index) in todos" v-bind:key="index">{{ item }}</div>

    <ul>
      <li v-for="(item, i) in todos" :key="i">{{ item }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      title: "탈주",
      num: "8.1",
      won: "11,000",
      todos: ["구교", "이제훈", "이옥섭"],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "./assets/css/style.scss";
</style>
