<template>

  <div class="menu">
    <a v-for="a in menuName" :key="a">{{ a }}</a>
  </div>

    <div>
    <h4>{{products[0]}}</h4>
    <p>70 만원</p>
    <button @click="increase">허위매물신고</button> <span>신고수 : {{ count }}</span>
  </div> 
    <div>
    <h4>{{products[1]}}</h4>
    <p>60 만원</p>
    <button @click="count2++">허위매물신고</button> <span>신고수 : {{ count2 }}</span>
  </div>
    <div>
    <h4>{{products[2]}}</h4>
    <p>70 만원</p>
    <button @click="count3++">허위매물신고</button> <span>신고수 : {{ count3 }}</span>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      count : 0,
      count2 : 0,
      count3 : 0,
      menuName : ['HOME', 'SHOP', 'ABOUT'],
      products : ['역삼동원룸', '천호동원룸', '마포구원룸']
    }
  },
  methods : {
    increase(){
      this.count += 1;
      console.log('함수 테스트')
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
  background: darkblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}
</style>
