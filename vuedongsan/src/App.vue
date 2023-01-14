<template>


  <div class="black-bg" v-if="modal == true">
    <div class="white-bg">
      <h4>상세페이지임</h4>
      <p>상세 페이지 내용임</p>
      <button @click="modal = false">닫기</button>
    </div>
  </div>

  <div class="menu">
    <a v-for="a in menuName" :key="a">{{ a }}</a>
  </div>

  <div v-for="(roomData, i) in oneRoom" :key="i">
    <img :src="oneRoom[i].image" class="room">
    <h4>{{oneRoom[i].title}}</h4>
    <p>{{oneRoom[i].price}} 원</p>
  </div> 
</template>

<script>

import data from './assets/data.js';

export default {
  name: 'App',
  data(){
    return{
      oneRoom : data,
      modal : false,
      count : [0, 0, 0],
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

.room {
  width: 20%;
  margin-top: 40px;
}

body {
  margin: 0;
}

div {
  box-sizing: border-box;
}

.black-bg {
  width: 100%; height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  position: fixed; padding: 20px;
}

.white-bg {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;
}
</style>
