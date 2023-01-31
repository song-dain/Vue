<template>
  <div>
    <div>
      <input
        type="radio"
        name=""
        id="html"
        value="HTML"
        v-model="favoritLang"
      />
      <label for="html">HTML</label>
    </div>
    <div>
      <input type="radio" name="" id="css" value="CSS" v-model="favoritLang" />
      <label for="css">CSS</label>
    </div>
    <div>
      <input type="radio" name="" id="js" value="JS" v-model="favoritLang" />
      <label for="js">JS</label>
    </div>
    <div>선택한 지역 : {{ favoritLang }}</div>
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      favoritLang: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
