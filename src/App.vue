<template>
  <div class="menu">
    <a v-for="(a, i) in products" :key="i">{{ a }}</a>
  </div>

  <div>
    <h4>{{ products[0] }}</h4>
    
    <p>{{ price1 }}won</p>
    <button @click="increase0">report</button>
    <span> report : {{ report1[0] }}</span>
  </div>
  <div>
    <h4>{{ products[1] }}</h4>
    <p>{{ price2 }}won</p>
    <button @click="increase1">report</button>
    <span> report : {{ report1[1] }}</span>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>{{ price2 }}won</p>
    <button @click="increase2">report</button>
    <span> report : {{ report1[2] }}</span>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      price1: 11,
      price2: 22,
      price3: 55,
      report1: [0, 0, 0],
      products: ["111", "222", "333", "444"],
    };
  },

  methods: {
    increase0() {
      this.report1[0]++;
    },
    increase1() {
      this.report1[1]++;
    },
    increase2() {
      this.report1[2]++;
    },
  },
  components: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.menu {
  background: darkslateblue;
  padding: 15px;
}

.menu a {
  color: white;
}
</style>
