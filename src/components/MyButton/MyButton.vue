<template>
  <div>
      <h2>我爱你们,亲爱的爸爸妈妈</h2>
      <button @click="count++">爱了{{count}}几次</button>
  </div>
</template>

<script>
export default {
  name: '',
  data(){
      return {
          count:0
      }
  }
}
</script>

<style scoped>
h2{
    color: wheat;
}
</style>
