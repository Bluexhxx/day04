<template>
  <div>
    <p>
      <span v-for="(item, index) in arr" :key="index">
        <input type="checkbox" v-model="newarr" :value="item" />
        {{ item }}
      </span>
    </p>
    <p>你选中的元素累加的和为： {{ sumAll }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: [9, 15, 19, 25, 29, 31, 48, 57, 62, 79, 87],
      newarr: [],
    };
  },
  computed: {
    sumAll(){
      return this.newarr.reduce((total,curr) => total += curr,0)
    }
  },
};
</script>

<style></style>
