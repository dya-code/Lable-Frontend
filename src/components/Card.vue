<script>
  import { defineComponent } from 'vue'

  export default defineComponent({
    name: 'Card',
    props: {
      title: String,
      img: String
    }
  })
</script>
  
<template>
  <div class="card p-10 m-10 w-[300px] bg-white rounded-3xl shadow-xl">
    <img class="card-img rounded-xl w-[250px] h-[320px] mb-8" :src="img">
    <div class="card-title font-bold text-2xl w-52 truncate">{{ title }}</div>
  </div>
</template>
  
<style scoped>
</style>  