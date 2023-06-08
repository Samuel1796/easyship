<script setup>
  import mNav from '@/components/mobile-nav.vue'
  import Navbar from '@/components/nav.vue';
  import shippingForm from '@/components/shipping-form.vue';

import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'
// initialize components based on data attribute selectors
onMounted(() => {
    initFlowbite();
})

</script>


<template>
  <mNav/>
    <div class="banner border bg-[#f5e6ed]">
      <Navbar/>
      <shippingForm/>

    </div>

<!-- Mobile nav -->
    
</template>
 
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
*{
  font-family: 'Montserrat', sans-serif;
}
  .banner{
    height: 125vh;
    width: 100vw;
    
  }


</style>


  