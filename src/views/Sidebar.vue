<template>
  <div>
    <h1>Vues示例</h1>
    <ul>
      <li>
        <router-link to="/example01">welcome</router-link>
      </li>
      <li>
        <router-link to="/example02">Data()</router-link>
      </li>
      <li>
        路由传参
        <ul>
          <li>
            <router-link to="/example03/students/42/homework/1">
              42,1
            </router-link>
          </li>
          <li>
            <router-link to="/example03/students/42/homework/2">
              42,2
            </router-link>
          </li>
        </ul>
      </li>
      <li>
        基本指令
        <ul>
          <li>
            <router-link to="/example04-01">v-text v-if v-show</router-link>
          </li>
          <li>
            <router-link to="/example04-02">v-bind</router-link>
          </li>
          <li>
            <router-link to="/example04-03">v-for</router-link>
          </li>
        </ul>
      </li>
      <li>
        双向绑定
        <ul>
          <li>
            <router-link to="/example05-01">v-module双向绑定</router-link>
          </li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<style scoped>
h1 {
  color: red;
}
ul {
  margin-top: 20px;
  margin-left: 30px;
}
ul ul {
  margin-top: 00px;
}
ul > li {
  margin-left: 10px;
}
</style>
