<template>
  <div class="about">
    <h1>Este es el perro!</h1>
    <div v-for="(dog, index) in dogs.message" :key="'Dogs' + index">
      <img :src="dog">
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'DogsParams',
  props: ['breedName'],
  data(){
    return{
      dogs: null
    }
  },
  async created(){
    let response = await axios.get('https://dog.ceo/api/breed/' + this.breedName + '/images');

    this.dogs = response.data;
  }
}
</script>

