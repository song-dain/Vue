<template>
  <div>
    <h1>Hellow {{ userName }}</h1>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userName: 'John Doe',
      message: 'Welcome 개발자의 품격'
    }
  }
}
</script>

<style scoped></style>
