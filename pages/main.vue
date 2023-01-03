<template>
  <div id="app">
    <p>메인 페이지입니다.</p>
    <ul>
      <li v-for="item in this.products" :key="item">{{ item }}</li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  data(){
    return{
      products : [],
    }
  },
  async created(){
    const response = await axios.get('http://localhost:3000/products');
    this.products = response.data;
  }
}
</script> 


<style>

</style>