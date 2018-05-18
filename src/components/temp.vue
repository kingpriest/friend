<template>
  <h1>{{message}}</h1>
</template>
<script>
export default {
  name:'temp',
  props:{
      message:String
  }
}
</script>
<style scoped>
  h1{
    background: red;
  }
</style>
