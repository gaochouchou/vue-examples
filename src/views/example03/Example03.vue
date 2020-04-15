<template>
  <div>
    <p>在router启用props支持。在vue props属性中声明同名变量</p>
    studentID: {{ sid }}
    <br />
    homeworksID: {{ hid }}
    <br />
    也可通过$route.params调用
    <br />
    {{ $route.params.sid }}
    <hr />
    {{ getTitle }}
  </div>
</template>
<script>
export default {
  props: ["sid", "hid"],
  data: () => ({
    homeworks: [
      { id: 1, title: "spring" },
      { id: 2, title: "springMVC" },
      { id: 3, title: "JPA" }
    ]
  }),
  created() {
    console.log("created");
  },
  // 第一次不会改变，数据改变后，要重新渲染时候会调用此方法
  beforeUpdate() {
    console.log("beforeupdate()");
  },
  // beforeRouteUpdate(to, from, next) {
  //   console.log("beforeRouterUpdate");
  //   // 不执行next方法，不会继续往下执行
  //   next();
  // },
  // beforeUpdate() {
  //   console.log("beforeUpdate()");
  // },
  // beforeRouteUpdate(to, from, next) {
  //   console.log("beforeRouterUpdate()");
  //   next();
  // },
  computed: {
    getTitle() {
      return this.homeworks.find(h => h.id == this.hid).title;
    }
  }
};
</script>
