<template>
  <div>
    <p>{{ msg }}</p>
    <p>{{ user.name }} / {{ replace }}</p>
    <p>
      计算属性，默认声明的是属性的getter方法，不支持传参。但JS中，属性可以是一个，函数
    </p>
    <p>{{ myReplace(user.insertTime) }}</p>
    <button @click="change">click</button>
  </div>
</template>
<script>
export default {
  //   data() {
  //     return {
  //       msg: "df",
  //       user: {
  //         name: "JIE"
  //       },
  //       courses: []
  //     };

  data: () => ({
    msg: "df",
    user: {
      name: "JIE",
      insertTime: "2020.04.09T08:30:21"
    },
    courses: []
  }),

  methods: {
    change() {
      this.user.name = "SUN";
    }
  },

  computed: {
    replace() {
      return this.user.insertTime.replace("T", " ");
    },
    myReplace() {
      return data => data.replace("T", " ");
    }
  }
};
</script>
