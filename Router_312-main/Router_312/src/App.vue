<script setup>

import { RouterView } from 'vue-router'
import boxheader from '@/views/boxheader.vue'
import JumboHead from './views/JumboHead.vue'
</script>


<template>
  <div class="container">
    <boxheader></boxheader>
    <JumboHead
      class="jumbo-head"
      text_title="Welcome to Gundam Unicorn Shop🤖"
      ex_box="Gundam Unicorn Shop🤖 แหล่งรวมกันดัมซีรี่ Unicorn มากมายเพราะเจ้าของเว็ปชอบซีรี่ย์นี้ซี่รี่ย์อื่นไม่มีนะครับ อิอิ :)"
    ></JumboHead>
    <RouterView />
  </div>
</template>

<script>
export default {
  name: 'App',
};
</script>

<style scoped>

.jumbotron {
  background-color: #007BFF;
  color: #fff; 
  padding: 2rem;
  border-radius: 15px; 
}

.display-4 {
  font-weight: bold; 
}

.lead {
  font-size: 1.25rem; 
}



body {
  background-color: #f8f9fa; 
}


.container {
  background-color: #fff;
  padding: px;
  border-radius: 10px; 
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
}





</style>