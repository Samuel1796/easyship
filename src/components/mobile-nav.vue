<script setup>
import { ref } from 'vue';
const isClosed = ref(true);

const toggleMenu = () => {
      isClosed.value = !isClosed.value;
    };
</script>

<template>
    <ul class="small__screen-menu">
        <div class="sm-icons" id="toggleMenu" @click="toggleMenu">
          <b>{{ isClosed ? 'Menu' : 'Close' }} </b>
          <svg class="w-6 h-6" aria-hidden="true" :class="{ 'rotate-180': !isClosed }" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
            <path v-if="isClosed" fill-rule="evenodd" d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z" clip-rule="evenodd"></path>
            <path v-else fill-rule="evenodd" d="M17 5a1 1 0 00-1-1H4a1 1 0 100 2h12a1 1 0 001-1zm0 5a1 1 0 00-1-1H4a1 1 0 100 2h12a1 1 0 001-1zm0 5a1 1 0 00-1-1H4a1 1 0 100 2h12a1 1 0 001-1z" clip-rule="evenodd"></path>
          </svg>
        </div>
        <div class="small__screen-menu-li" :class="{ hide: isClosed }" id="closeContainer">
          <router-link to="/"><li class="">Home</li></router-link>
          <a href="#about"><li class=""> About Us</li></a>
          <a href="#services"><li class="">Services</li></a>
          <a href="#resources"><li class="">Resources</li></a>
        </div>
      </ul>
</template>

<style scoped>


.small__screen-menu {
    z-index: 999;
  }
  
  
  
  
  .small__screen-menu li {
    padding-top: 1.5rem;
    padding-left: 5rem;
    padding-right: 5rem;
    margin-left: 0.5rem;
    margin-right: 0.5rem;
    color: #f5e6ed;
    background-color: black;
  
  }
  
  
  
  .small__screen-menu-li {
    margin-bottom: 0.5em;
    padding-top: 1rem;
    border-radius: 30%;
    transition: opacity 0.3s ease-in-out, transform 0.3s ease-in-out;
    border-radius: 0.5rem;
  
  
  }
  .hide {
      opacity: 0;
      transform: translateX(100%);
    }
    
  .small__screen-menu li {
    padding: 1rem 2.3rem;
  }
  
  
  .small__screen-menu {
    margin-right: 1rem;
    display: none;
    margin-bottom: 2rem;
    margin-right: 2rem;
  }
  
  .sm-icons {
    padding-left: 1rem;
    padding-right: 1rem;
    padding-top: 0.25rem;
    padding-bottom: 0.25rem;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.25rem;
    background-color: black;
    border-radius: 0.5rem;
    width: 8rem;
    color:#f5e6ed;
  }
  
  
  
  
  
  
  @media screen and (max-width: 600px) {
    
  
    .small__screen-menu {
      display: flex;
      flex-direction: column-reverse;
      align-items: flex-end;
      position: fixed;
      bottom: 0;
      right: 0;
    }
  
   
  }
</style>