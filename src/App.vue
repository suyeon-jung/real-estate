<template>
    <div class="menu">
        <a v-for="(menu, idx) in menus" :key="idx">{{menu}}</a>
    </div>

  <div>
      <h4>{{products[0]}}</h4>
      <p>{{prices[0]}}</p>
      <button @click="increase(0)">허위매물 신고</button> <span>신고수 : {{신고수[0]}}</span>
  </div>
  <div>
      <h4>{{products[1]}}</h4>
      <p>{{prices[1]}}</p>
      <button @click="increase(1)">허위매물 신고</button> <span>신고수 : {{신고수[1]}}</span>

  </div>
  <div>
      <h4>{{products[2]}}</h4>
      <p>{{prices[2]}}</p>
      <button @click="increase(2)">허위매물 신고</button> <span>신고수 : {{신고수[2]}}</span>
  </div> 
</template>

<script>


export default {
  name: 'App',
  data(){
      return {
          신고수 : [0, 0, 0],
          menus : ["Home", "Shop", "About"],
          products: ["역삼동원룸", "천호동원룸", "마포구원룸"],
          prices: ["50만원", "60만원", "70만원"]
      }
  },
  methods:{
      increase(idx){
          this.신고수[idx] += 1;
      }
  },
  components: {

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
    background: darkslateblue;
    padding: 15px;
    border-radius:  5px;
}

.menu a {
    color: white;
    padding:  10px;
}
</style>
