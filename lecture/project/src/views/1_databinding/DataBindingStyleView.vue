<template>
  <div>
    <div :style="style">스타일 바인딩 : 글씨는 red, 폰트크기 : 30px</div>
    <div :style="style2">스타일 바인딩 : 글씨는 green, 폰트크기 : 30px</div>
    <button @click="style.color = 'blue'">색상바꾸기</button>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      style: {
        color: 'red',
        fontSize: '30px'
      },
      style2: {
        color: 'green',
        fontSize: '30px'
      }
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
