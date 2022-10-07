<script>
  import { defineComponent } from 'vue'

  export default defineComponent({
    name: 'Nav'
  })
</script>
  
<template>
  <nav class="w-screen h-20 bg-white rounded-b-3xl shadow-2xl fixed flex items-center mb-">
    <div class="nav-title ml-10 mr-10 font-extrabold text-3xl text-transparent bg-clip-text bg-gradient-to-r from-purple-400 to-pink-600">Lable</div>
    <a class="nav-item ml-10 font-bold text-xl text-transparent bg-clip-text bg-gradient-to-r from-purple-400 to-pink-600 hover:text-blue-400" href="/">검색</a>
    <a class="nav-item ml-10 font-bold text-xl text-transparent bg-clip-text bg-gradient-to-r from-purple-400 to-pink-600 hover:text-blue-400" href="/">깃허브</a>
  </nav>
</template>
  
<style scoped>
</style>  