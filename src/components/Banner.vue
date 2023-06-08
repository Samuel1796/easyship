<script setup>
import Navbar from '@/components/nav.vue';
import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'
// initialize components based on data attribute selectors
onMounted(() => {
    initFlowbite();
})

</script>




<template>
    <!-- Your existing navbar code goes here -->
    <Navbar/>
  
  <div id="home" class="bg-[#f5e6ed]">
     <div class=" bg-[#f5e6ed] container mx-auto px-4 mt-28 main">
      <div class="flex flex-wrap mt-8 bg-[#f5e6ed]">
        <div class="w-full sm:w-1/2 lg:w-1/3 px-4  lg:pl-15">
          <div class="bg-[#f5e6ed] p-6">
            <!-- Content for the first container goes here -->
            
            <p class="max-w-lg lg:pt-20 lg:text-4xl text-3xl font-semibold text-gray-900">Lorem ipsum dolor sit<br> amet consectetur, adipisicing elit.</p>
            <p class="max-w-lg   py-4">Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
            <router-link to="/forms">
              <v-btn height="42" min-width="200" rounded="xl">
              <p class="font-semibold ">Get Started</p>
            </v-btn>
          </router-link>
          </div>
        </div>

        <div class="w-full sm:w-1/2 lg:w-2/3 px-4 mb-8">
            <div class="bg-[#f5e6ed]  p-10">
              <video autoplay loop muted>
                <source src="@/assets/bggg.mp4" type="video/mp4">
                Your browser does not support the video tag.
              </video>
              <!-- Content for the second container goes here -->
            </div>
          </div>
          
      </div>
    </div>




  <!-- ABOUT -->

  <section id="about" class="bg-white dark:bg-gray-900 relative">
    <div class="py-8 px-4 mx-auto max-w-screen-xl text-center lg:py-16 z-10 relative">
      <h1 class="mb-4 text-4xl font-extrabold tracking-tight leading-none text-gray-900 md:text-5xl lg:text-6xl dark:text-white">Easyship is Built for Your Business</h1>
      <p class="mb-8 text-lg font-normal text-gray-500 lg:text-xl sm:px-16 lg:px-48 dark:text-gray-200">We work around the clock to get your shipments to the right place at the right time.</p>

      <div class=" bg-transparent container mx-auto p-8 mt-auto main">

                <!-- Content for the first container goes here -->


                            
                <div id="accordion-color" data-accordion="collapse" data-active-classes="bg-blue-100 dark:bg-gray-800 text-blue-600 dark:text-white">
                  <h2 id="accordion-color-heading-1">
                    <button type="button" class="flex items-center justify-between w-full p-5 font-medium text-left text-gray-500 border border-b-0 border-gray-200 rounded-t-xl focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800" data-accordion-target="#accordion-color-body-1" aria-expanded="true" aria-controls="accordion-color-body-1">
                      <span>What is EasyShip?</span>
                      <svg data-accordion-icon class="w-6 h-6 rotate-180 shrink-0" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                    </button>
                  </h2>
                  <div id="accordion-color-body-1" class="hidden" aria-labelledby="accordion-color-heading-1">
                    <div class="p-5 border border-b-0 border-gray-200 dark:border-gray-700 dark:bg-gray-900">
                      <p class="mb-2 text-gray-500 dark:text-gray-400">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quae ducimus impedit veniam quam rem, explicabo, ipsam provident cum odio unde fuga minus accusamus illum ab numquam. Voluptates assumenda beatae voluptas!</p>
                    </div>
                  </div>
                  <h2 id="accordion-color-heading-2">
                    <button type="button" class="flex items-center justify-between w-full p-5 font-medium text-left text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800" data-accordion-target="#accordion-color-body-2" aria-expanded="false" aria-controls="accordion-color-body-2">
                      <span>How long have we been operating?</span>
                      <svg data-accordion-icon class="w-6 h-6 shrink-0" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                    </button>
                  </h2>
                  <div id="accordion-color-body-2" class="hidden" aria-labelledby="accordion-color-heading-2">
                    <div class="p-5 border border-b-0 border-gray-200 dark:border-gray-700">
                      <p class="mb-2 text-gray-500 dark:text-gray-400">Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque deserunt nam vitae quasi maxime sit nesciunt recusandae alias officia eos? Ipsum at dolorem laborum amet repellendus a cum maxime quia?</p>
                    </div>
                  </div>
                  <h2 id="accordion-color-heading-3">
                    <button type="button" class="flex items-center justify-between w-full p-5 font-medium text-left text-gray-500 border border-gray-200 focus:ring-4 focus:ring-blue-200 dark:focus:ring-blue-800 dark:border-gray-700 dark:text-gray-400 hover:bg-blue-100 dark:hover:bg-gray-800" data-accordion-target="#accordion-color-body-3" aria-expanded="false" aria-controls="accordion-color-body-3">
                      <span>Who are our affiliates?</span>
                      <svg data-accordion-icon class="w-6 h-6 shrink-0" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                    </button>
                  </h2>
                  <div id="accordion-color-body-3" class="hidden" aria-labelledby="accordion-color-heading-3">
                    <div class="p-5 border border-t-0 border-gray-200 dark:border-gray-700">
                      <p class="mb-2 text-gray-500 dark:text-gray-400">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quibusdam alias, a exercitationem doloribus qui itaque dicta, ipsa accusantium assumenda doloremque tenetur laborum nostrum non sint! Voluptas corrupti nemo quidem optio.</p>
                      
                    </div>
                  </div>
                </div>

               </div>
                
    
           
              
         
      </div>
    

    <div class="absolute top-0 left-0 w-full h-full z-0">
      <div class="bg-gradient-to-b from-[#f5e6ed] to-white w-full h-full"></div>
    </div>
  </section>



  <!-- SERVICES -->
  
  <section id="services" class="bg-white dark:bg-gray-900 relative">
    <div class="py-8 px-4 mx-auto max-w-screen-xl text-center lg:py-16 z-10 relative">
      <h1 class="mb-4 text-4xl font-extrabold tracking-tight leading-none text-gray-900 md:text-5xl lg:text-6xl dark:text-white">Access Our Network of Global Warehouses</h1>
      <p class="mb-8 text-lg font-normal text-gray-500 lg:text-xl sm:px-16 lg:px-48 dark:text-gray-200">If you're not thinking internationally for your eCommerce business, you're depriving customers who want to buy your products.
         Easyship strives to make shipping to 220+ countries as seamless as domestic.</p>

        
        <div class=" bg-transparent container mx-auto px-4 mt-auto main">
          <div class="flex flex-wrap mt-8 bg-transparent">
            <div class="w-full sm:w-1/2 lg:w-1/3 px-2  lg:pl-15">
              <div class="bg-transparent lg:p-6">
                <!-- Content for the first container goes here -->

                <p class="max-w-lg lg:pt-20 lg:text-4xl text-3xl font-semibold text-gray-900">Don't Pay Unnecessary Tariffs</p>
                 <p class="max-w-lg   py-4">Your fulfillment strategy is likely costing you money in unnecessary tariffs and the China-US Trade War will likely increase that. We offer shipping services that allow you to reduce your tariff exposure
                   in addition to streamlining your logistics supply chain by being close to source.</p>

              </div>
            </div>
    
    
            <div class=" w-full sm:w-1/2 lg:w-2/3 px-4 mb-8">
                <div class="bg-transparent  p-10">
                  
                  <!-- Content for the second container goes here -->
                  <img src="@/assets/service1.avif" alt="">

                
                </div>
            </div>
              
          </div>

          <hr class="bg-black">

          <div class="flex flex-wrap mt-8 bg-transparent">
            <div class="w-full sm:w-1/2 lg:w-2/3 px-2  lg:pl-15">
              <div class="bg-transparent lg:p-6">
                <!-- Content for the first container goes here -->
                <video autoplay loop muted>
                  <source src="@/assets/servive3.mp4" type="video/mp4">
                  Your browser does not support the video tag.
                </video>

               

              </div>
            </div>
    
    
            <div class=" w-full sm:w-1/2 lg:w-1/3 px-4 mb-8">
                <div class="bg-transparent  p-10">
                  
                  <!-- Content for the second container goes here -->
                  <p class="max-w-lg lg:pt-20 lg:text-4xl text-3xl font-semibold text-gray-900">Flawless Tracking and Returns</p>
                  <p class="max-w-lg   py-4">Maintain visibility of packages with real time accurate tracking for all couriers. Share tracking info on a dedicated professional tracking page. </p>

                
                </div>
            </div>
              
          </div>


          
        </div>
      </div>
    

    <div class="absolute top-0 left-0 w-full h-full z-0">
      <div class="bg-gradient-to-b from-[#f5e6ed] to-white w-full h-full"></div>
    </div>
  </section>



  <!-- RESOURCES -->
  
  <section id="resources" class="bg-white dark:bg-gray-900 relative">
    <div class="py-8 px-4 mx-auto max-w-screen-xl text-center lg:py-16 z-10 relative">
      <h1 class="mb-4 text-2xl font-extrabold tracking-tight leading-none text-gray-900 md:text-3xl lg:text-4xl dark:text-white">Frequently Asked Questions</h1>
      <p class="mb-8 text-lg font-normal text-gray-500 lg:text-xl sm:px-16 lg:px-48 dark:text-gray-200">We work around the clock to get your shipments to the right place at the right time.</p>

        
        <div class=" bg-transparent container mx-auto px-4 mt-auto main">
          
                      
            <div id="accordion-arrow-icon" data-accordion="open">
              <h2 id="accordion-arrow-icon-heading-1">
                <button type="button" class="flex items-center justify-between w-full p-5 font-medium text-left text-gray-900 bg-gray-100 border border-b-0 border-gray-200 rounded-t-xl focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-white dark:bg-gray-800 hover:bg-gray-100 dark:hover:bg-gray-800" data-accordion-target="#accordion-arrow-icon-body-1" aria-expanded="true" aria-controls="accordion-arrow-icon-body-1">
                  <span>What issues could I encounter when shipping overseas?</span>
                </button>
              </h2>
              <div id="accordion-arrow-icon-body-1" aria-labelledby="accordion-arrow-icon-heading-1">
                <div class="p-5 border border-b-0 border-gray-200 dark:border-gray-700 dark:bg-gray-900">
                  <p class="mb-2 text-gray-500 dark:text-gray-400">
                    Some countries are easier to ship to than others. For example, India requires more personal documentation from the receiver than most countries. In Brazil, there are multiple taxes and duties that are imposed on imports. Economic instability makes delivery even more complicated.
                    Being aware of these potential issues will allow you manage expectations and build trust with your overseas customers
                  </p>
                </div>
              </div>

              <h2 id="accordion-arrow-icon-heading-2">
                <button type="button" class="flex items-center justify-between w-full p-5 font-medium text-left text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800" data-accordion-target="#accordion-arrow-icon-body-2" aria-expanded="false" aria-controls="accordion-arrow-icon-body-2">
                  <span>Can I import my product to my target countries?</span>
                  <svg data-accordion-icon class="w-6 h-6 shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 13l-3 3m0 0l-3-3m3 3V8m0 13a9 9 0 110-18 9 9 0 010 18z"></path></svg>
                </button>
              </h2>
              <div id="accordion-arrow-icon-body-2" class="hidden" aria-labelledby="accordion-arrow-icon-heading-2">
                <div class="p-5 border border-b-0 border-gray-200 dark:border-gray-700">
                  <p class="mb-2 text-gray-500 dark:text-gray-400">Start by visiting the official customs
                    website for the countries you'd like to ship to and take a look at the prohibited and restricted items.
                    Products such as plants, seeds, alcoholic beverages, food products, 
                    and more could potentially be quarantined in customs for a long period of time, or be outright prohibited.
                  </p>
                </div>
              </div>

              <h2 id="accordion-arrow-icon-heading-3">
                <button type="button" class="flex items-center justify-between w-full p-5 font-medium text-left text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800" data-accordion-target="#accordion-arrow-icon-body-3" aria-expanded="false" aria-controls="accordion-arrow-icon-body-3">
                  <span>Does my product contain dangerous goods?</span>
                  <svg data-accordion-icon class="w-6 h-6 shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 13l-3 3m0 0l-3-3m3 3V8m0 13a9 9 0 110-18 9 9 0 010 18z"></path></svg>
                </button>
              </h2>
              <div id="accordion-arrow-icon-body-3" class="hidden" aria-labelledby="accordion-arrow-icon-heading-3">
                <div class="p-5 border border-b-0 border-gray-200 dark:border-gray-700">
                  <p class="mb-2 text-gray-500 dark:text-gray-400">In the shipping world, dangerous goods can be anything that, if not handled with care, could harm those handling them in transit.

                    Batteries and liquids are a good example: they are not dangerous by themselves, but they can contain a dangerous component (such as being flammable.) Couriers must be aware if your shipment contains these materials so they can handle them carefully.</p>
                </div>
              </div>

              <h2 id="accordion-arrow-icon-heading-4">
                <button type="button" class="flex items-center justify-between w-full p-5 font-medium text-left text-gray-500 border border-b-0 border-gray-200 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-800 dark:border-gray-700 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800" data-accordion-target="#accordion-arrow-icon-body-4" aria-expanded="false" aria-controls="accordion-arrow-icon-body-4">
                  <span>What to do when your shipment is stuck in customs</span>
                  <svg data-accordion-icon class="w-6 h-6 shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 13l-3 3m0 0l-3-3m3 3V8m0 13a9 9 0 110-18 9 9 0 010 18z"></path></svg>
                </button>
              </h2>
              <div id="accordion-arrow-icon-body-4" class="hidden" aria-labelledby="accordion-arrow-icon-heading-4">
                <div class="p-5 border border-b-0 border-gray-200 dark:border-gray-700">
                  <p class="mb-2 text-gray-500 dark:text-gray-400">There are many reasons why a shipment might be stuck at customs. The reasons can differ in severity from high (your goods are prohibited) to low (having the incorrect paperwork).

                    Here's what you can do to get your parcel out of customs limbo:<br>
                    
                    <b>Contact your courier directly.</b> Express couriers can help customs clear your shipment<br>
                    <b>Find out if there are any outstanding taxes to be paid.</b> Arrange payment and settle the balance ASAP<br>
                    <b>Ensure there is no missing or incorrect paperwork.</b> Express couriers might be able to help you recover any missing paperwork<br>
                  </p>
                </div>
              </div>
              
            </div>
        </div>
      </div>
    

    <div class="absolute top-0 left-0 w-full h-full z-0">
      <div class="bg-gradient-to-b from-[#f5e6ed] to-white w-full h-full border"></div>
    </div>


         <div class=" bg-[#f5e6ed] border container mx-auto px-4 mt-28 main">
          </div>
  </section>

  
<footer class="bg-white rounded-lg shadow dark:bg-gray-900 m-4">
  <div class="w-full max-w-screen-xl mx-auto p-4 md:py-8">
      <div class="sm:flex sm:items-center sm:justify-between">
          <a href="#home" class="flex items-center mb-4 sm:mb-0">
              <span class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white">Easyship</span>
          </a>
          <ul class="flex flex-wrap items-center mb-6 text-sm font-medium text-gray-500 sm:mb-0 dark:text-gray-400">
              <li>
                  <a href="#about" class="mr-4 hover:underline md:mr-6 ">About</a>
              </li>
              <li>
                  <a href="#services" class="mr-4 hover:underline md:mr-6">Services</a>
              </li>
              <li>
                  <a href="#resources" class="mr-4 hover:underline md:mr-6 ">Resources</a>
              </li>
              
          </ul>
      </div>
      <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" />
      <div class="sm:flex sm:items-center sm:justify-between">
        <span class="text-sm text-gray-500 sm:text-center dark:text-gray-400">© 2023 <a href="#home" class="hover:underline">Easyship™</a>. All Rights Reserved.
        </span>
        <div class="flex mt-4 space-x-6 sm:justify-center sm:mt-0">
            <a href="#" class="text-gray-500 hover:text-gray-900 dark:hover:text-white">
                <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z" clip-rule="evenodd" /></svg>
                <span class="sr-only">Facebook page</span>
            </a>
            <a href="#" class="text-gray-500 hover:text-gray-900 dark:hover:text-white">
                <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z" clip-rule="evenodd" /></svg>
                <span class="sr-only">Instagram page</span>
            </a>
            <a href="#" class="text-gray-500 hover:text-gray-900 dark:hover:text-white">
                <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84" /></svg>
                <span class="sr-only">Twitter page</span>
            </a>
            <a href="#" class="text-gray-500 hover:text-gray-900 dark:hover:text-white">
                <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd" /></svg>
                <span class="sr-only">GitHub account</span>
            </a>
            
        </div>
    </div>
  </div>
</footer>





</div>

</template>






<style scoped>
*{
  scroll-behavior: smooth;
}

/* Your custom styles for the component go here */

</style>
