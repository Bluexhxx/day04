<template>
  <table class="table table-bordered">
    <caption>
      欢迎光临vue开发的收银系统-水果店
    </caption>
    <thead>
      <tr>
        <th>苹果10元/斤，折扣：<8折></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th>
          请输入你要购买的斤数<input type="number" v-model.number="weight" min="0" />
        </th>
      </tr>
      <tr>
        <th>
          <button type="button" class="btn btn-success btn-sm" @click="pay">
            结账买单
          </button>
        </th>
      </tr>
      <tr>
        <th>
          结账单：总价：{{ weight2 * 10 }} ￥元，折后价{{
            weight2 * 8
          }}，省了：{{ weight2 * 2 }} ￥元
        </th>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  data() {
    return {
      weight: 0,
      weight2: 0,
    };
  },
  methods: {
    pay() {
      this.weight2 = this.weight
    },
  },
};
</script>

<style>
table {
  caption-side: top !important;
}
.table th,
.table td,
.table caption {
  text-align: center;

  height: 38px;
}
</style>
