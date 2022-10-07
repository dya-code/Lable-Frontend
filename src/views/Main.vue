<script>
  import { defineComponent } from 'vue'
  import axios from 'axios'

  import Card from '../components/Card.vue'
  import Nav from '../components/Navbar.vue'

  export default defineComponent({
    components: {
      Card,
      Nav
    },
    data: () => {
      return {
        res: []
      }
    },
    methods: {
    },
    async mounted() {
      await axios.get('http://localhost:3000/api/timetable/').then( resp => this.res = resp.data )

      console.log(this.res[0].img)
    }
  })
</script>

<template>

  <div>
    <Nav />

    <div class="img flex justify-center items-center">
      <img class="absolute -z-10 hellobg object-cover w-screen h-[1000px] mt-[800px]" src="../assets/hellobg.png">
      <div class="absolute -z-10 title font-extrabold text-8xl mt-[900px]">LABLE</div>
    </div>

    <div class="flex justify-center items-center flex-wrap ml-[200px] mr-[200px] mt-[1000px]">
      <Card v-for="item in res" v-bind:title="item.title" v-bind:img="item.img" />
    </div>

  </div>
</template>
  
<style scoped>
</style>