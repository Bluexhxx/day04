<template>
  <div>
    <p>
      <span v-for="(item, index) in arr" :key="index">
        <input type="checkbox" v-model="newarr" :value="item" />
        {{ item }}
      </span>
    </p>
    <ul>
      <li v-for="(item, index) in newarr" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: ["科幻", "喜剧", "动漫", "冒险", "科技", "军事", "娱乐", "奇闻"],
      newarr: [],
    };
  },
};
</script>

<style></style>
