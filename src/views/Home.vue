<script setup>
  import Banner from '@/components/Banner.vue';
  import mNav from '@/components/mobile-nav.vue'

</script>


<template>
  <mNav/>
    <div class="banner border bg-[#f5e6ed]">
      <Banner/>

    </div>

<!-- Mobile nav -->
    
</template>
 
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');
*{
  font-family: 'Montserrat', sans-serif;
}
  .banner{
    height: 38em;
    width: 100vw;
    
  }


</style>

