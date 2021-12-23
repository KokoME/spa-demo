<template>
  <div class="about">
    <h1>Este es el perro!</h1>
    <img :src="dogOfDay.message">
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'Dogs',
  data(){
    return{
      dogOfDay: null
    }
  },
  async created(){
    let response = await axios.get('https://dog.ceo/api/breeds/image/random');
    this.dogOfDay = response.data;
  }
}
</script>

