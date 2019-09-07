<template>
  <div class="home">
    <Pin msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Pin from '@/components/Pin.vue'

export default {
  name: 'home',
  components: {
    Pin
  }
}
</script>

<style scoped>
.home{
  display: inline-block;
}
</style>