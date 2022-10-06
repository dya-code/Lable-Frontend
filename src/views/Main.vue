<script>
  import { defineComponent } from 'vue'
  import axios from 'axios'

  import Card from '../components/Card.vue'

  export default defineComponent({
    components: {
      Card
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
    <div class="title m-20 flex justify-center font-bold text-white text-5xl">Daily</div>
  
    <div class="flex justify-center items-center flex-wrap ml-[200px] mr-[200px]">
      <Card v-for="item in res" v-bind:title="item.title" v-bind:img="item.img" />
    </div>
  </div>
</template>
  
<style scoped>
</style>