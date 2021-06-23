<template>
  <div class="home">
    <button @click="test">Test</button>
    <button @click="test1">Test1</button>
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
  methods: {
    test() {
      const api = `/test`;
      this.$http.get(api).then((response) => {
        console.log(response);
      });
    },
    test1() {
      const api1 = `/test1`;
      this.$http.get(api1).then((response) => {
        console.log(response);
      });
    }
  },
};
</script>
