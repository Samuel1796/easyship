<script setup>
// UI LIBRARY DEFAULT
import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'
import { ref } from 'vue';


// HANDLES ACTIVE TAB STYLING
const activeTab = ref('');
const changeTab = (tab) => {
      activeTab.value = tab;
    };

// initialize components based on data attribute selectors
onMounted(() => {
    initFlowbite();
})

</script>


<template>

    <div>
<nav class="bg-[#f5e6ed]  fixed w-full z-20 top-0 left-0 border-b border-gray-200">
    <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
    <a href="#home" class="flex items-center">
        <span class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white">Easyship</span>
    </a>
    <div class="flex md:order-2">

    
      <router-link to="/forms">
        <v-btn height="52" min-width="164" rounded="xl">
        <p class="font-semibold ">Get Started</p>
      </v-btn>
    </router-link>

    </div>
    <div class="items-center justify-between hidden w-full md:flex md:w-auto md:order-1" id="navbar-sticky">
        <ul class="flex flex-col p-4 md:p-0 mt-4 font-medium md:flex-row md:space-x-8 md:mt-0 md:bg-[#f5e6ed]">
          <li :class="{ 'active': activeTab === 'home' }">
            <router-link to="/" @click="changeTab('home') " class="font-semibold block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-blue-700 md:p-0" aria-current="page">Home</router-link>
          </li>
          <li :class="{ 'active': activeTab === 'about' }">
            <a href="#about" @click="changeTab('about')" class="font-semibold block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-blue-700 md:p-0">About</a>
          </li>
          <li :class="{ 'active': activeTab === 'services' }">
            <a href="#services" @click="changeTab('services')" class="font-semibold block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-blue-700 md:p-0">Services</a>
          </li>
          <li :class="{ 'active': activeTab === 'resources' }">
            <a href="#resources" @click="changeTab('resources')" class="font-semibold block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-blue-700 md:p-0">Resources</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
 
</div>
  

  
</template>


<style scoped>

li.active::after {
  content: "";
  display: block;
  width: 100%;
  height: 2px;
  background-color: #38b2ac;
  transform: scaleX(0);
  transition: transform 0.3s ease-in-out;
}

li.active:hover::after {
  transform: scaleX(1);
}

li.active a {
  color: #38b2ac;
}


</style>
