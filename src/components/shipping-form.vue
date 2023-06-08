<script setup>
import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'
// initialize components based on data attribute selectors
onMounted(() => {
    initFlowbite();
})

// SAVING INPUT
import { ref,reactive,computed } from 'vue';
//Form 1
const UserData = reactive({
      Name: '',
      Email: '',
      GPS: '',
      PAddress: '',
      Phone: '',
    });
    
const ShippingType = ref('');

    


    //Step Navigation
    const currentTab = ref(0);
    const steps = ref(['step1', 'step2', 'step3', 'step4']); // Replace with your actual steps
    // Step navigation methods
    const nextStep = ()=>{
        currentTab.value += 1;
    }
    const previousStep = ()=>{
        currentTab.value -= 1;
    }


// handles the payment sectiom
    const cardholder = ref('');
    const cardNumber = ref('');
    const expired = ref({
      month: '',
      year: '',
    });
    const securityCode = ref('');
    const card = ref('front');

   

    const format = () => {
      if (cardNumber.value.length > 18) {
        return;
      }
      cardNumber.value = cardNumber.value.replace(/\W/gi, '').replace(/(.{4})/g, '$1 ');
    };

    
// end


// Selected items
const items = [
      { id: 'car', name: 'Car', location: 'From Ohio' },
      { id: 'helicopter', name: 'Helicopter', location: 'From Utah' },
      { id: 'ship', name: 'Ship', location: 'From Miami' },
    ];
    const selectedItems = ref([]);
    const selectedNames = computed(() => {
        return selectedItems.value.map(item => item.name).join(', ');
    });
</script>



<template>
    

    <div class="  container mx-auto px-4 mt-28 main">

        <div v-for="(step, index) in steps" :key="index" class="step" v-show="currentTab === index">

        <ol class="flex items-center w-full mb-4 sm:mb-5">
            <li class="flex w-full items-center text-blue-600 dark:text-blue-500 after:content-[''] after:w-full after:h-1 after:border-b after:border-blue-100 after:border-4 after:inline-block dark:after:border-blue-800">
              <div class="flex items-center justify-center w-10 h-10 bg-blue-100 rounded-full lg:h-12 lg:w-12 dark:bg-blue-800 shrink-0">
                <svg v-if="index===0" aria-hidden="true" class="w-8 h-8 text-blue-600 lg:w-10 lg:h-10 dark:text-blue-300" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                  <path fill-rule="evenodd" d="M10 2a1 1 0 00-1 1v1a1 1 0 002 0V3a1 1 0 00-1-1zM4 4h3a3 3 0 006 0h3a2 2 0 012 2v9a2 2 0 01-2 2H4a2 2 0 01-2-2V6a2 2 0 012-2zm2.5 7a1.5 1.5 0 100-3 1.5 1.5 0 000 3zm2.45 4a2.5 2.5 0 10-4.9 0h4.9zM12 9a1 1 0 100 2h3a1 1 0 100-2h-3zm-1 4a1 1 0 011-1h2a1 1 0 110 2h-2a1 1 0 01-1-1z" clip-rule="evenodd"></path>
                </svg>
                <svg v-else aria-hidden="true" class="w-8 h-8 text-blue-600 lg:w-10 lg:h-10 dark:text-blue-300" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                    <path fill-rule="evenodd" d="M10 2a1 1 0 00-1 1v1a1 1 0 002 0V3a1 1 0 00-1-1zM4 4h3a3 3 0 006 0h3a2 2 0 012 2v9a2 2 0 01-2 2H4a2 2 0 01-2-2V6a2 2 0 012-2zm2.5 7a1.5 1.5 0 100-3 1.5 1.5 0 000 3zm2.45 4a2.5 2.5 0 10-4.9 0h4.9zM12 9a1 1 0 100 2h3a1 1 0 100-2h-3zm-1 4a1 1 0 011-1h2a1 1 0 110 2h-2a1 1 0 01-1-1z" clip-rule="evenodd"></path>
                  </svg>
              </div>
            </li>
            <li class="flex w-full items-center after:content-[''] after:w-full after:h-1 after:border-b after:border-gray-100 after:border-4 after:inline-block dark:after:border-gray-700">
              <div class="flex items-center justify-center w-10 h-10 bg-blue-100 rounded-full lg:h-12 lg:w-12 dark:bg-gray-700 shrink-0">
                <svg v-if="index === 1" aria-hidden="true" class="w-8 h-8 text-blue-600 lg:w-10 lg:h-10 dark:text-blue-300" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                  <path fill-rule="evenodd" d="M4 4a2 2 0 00-2 2v1h16V6a2 2 0 00-2-2H4z"></path>
                  <path fill-rule="evenodd" d="M18 9H2v5a2 2 0 002 2h12a2 2 0 002-2V9zM4 13a1 1 0 011-1h1a1 1 0 110 2H5a1 1 0 01-1-1zm5-1a1 1 0 100 2h1a1 1 0 100-2H9z" clip-rule="evenodd"></path>
                </svg>
                <svg v-else aria-hidden="true" class="w-8 h-8 text-gray-500 lg:w-10 lg:h-10 dark:text-gray-100" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                  <path d="M4 4a2 2 0 00-2 2v1h16V6a2 2 0 00-2-2H4z"></path>
                  <path fill-rule="evenodd" d="M18 9H2v5a2 2 0 002 2h12a2 2 0 002-2V9zM4 13a1 1 0 011-1h1a1 1 0 110 2H5a1 1 0 01-1-1zm5-1a1 1 0 100 2h1a1 1 0 100-2H9z" clip-rule="evenodd"></path>
                </svg>
              </div>
            </li>
            <li class="flex w-full items-center after:content-[''] after:w-full after:h-1 after:border-b after:border-gray-100 after:border-4 after:inline-block dark:after:border-gray-700">
              <div class="flex items-center justify-center w-10 h-10 bg-blue-100 rounded-full lg:h-12 lg:w-12 dark:bg-gray-700 shrink-0">
                <svg v-if="index === 2" aria-hidden="true" class="w-8 h-8 text-blue-600 lg:w-10 lg:h-10 dark:text-blue-300" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                  <path fill-rule="evenodd" d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                  <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm3 4a1 1 0 000 2h.01a1 1 0 100-2H7zm3 0a1 1 0 000 2h3a1 1 0 100-2h-3zm-3 4a1 1 0 100 2h.01a1 1 0 100-2H7zm3 0a1 1 0 100 2h3a1 1 0 100-2h-3z" clip-rule="evenodd"></path>
                </svg>
                <svg v-else aria-hidden="true" class="w-8 h-8 text-gray-500 lg:w-10 lg:h-10 dark:text-gray-400" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                  <path d="M9 2a1 1 0 000 2h2a1 1 0 100-2H9z"></path>
                  <path fill-rule="evenodd" d="M4 5a2 2 0 012-2 3 3 0 003 3h2a3 3 0 003-3 2 2 0 012 2v11a2 2 0 01-2 2H6a2 2 0 01-2-2V5zm9.707 5.707a1 1 0 00-1.414-1.414L9 12.586l-1.293-1.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
                </svg>
              </div>
            </li>
            
          </ol>
          


    <!-- Step 1 -->
<div v-if="index === 0">
    <form action="#" >
        <h3 class="mb-4 text-lg font-bold leading-none text-gray-900 dark:text-white">Personal Details</h3>
        <div class="grid gap-4 mb-4 sm:grid-cols-2">
            <div>
                <label for="username" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"><b>Username</b></label>
                <input v-model="UserData.Name" type="text" name="username" id="username" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-600 focus:border-blue-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="username.example" required="">
            </div>
            <div>
                <label for="email" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"><b>Email</b></label>
                <input v-model="UserData.Email" type="email" name="email" id="email" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-600 focus:border-blue-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="name@company.com" required="">
            </div>
            <div>
                <label for="gps" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"><b>GPS Address</b></label>
                <input v-model="UserData.GPS" type="text" name="gps" id="gps" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-600 focus:border-blue-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="gps-address.example" required="">
            </div>
            <div>
                <label for="address2" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"><b>Postal Address</b> </label>
                <input v-model="UserData.PAddress" type="text" name="address2" id="address2" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-600 focus:border-blue-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="postal-address.example" required="">
            </div>
            <div>
                <label for="phone" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"><b>Phone Number</b></label>
                <input v-model="UserData.Phone" type="tel" name="tel" id="tel" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-600 focus:border-blue-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="0XXXXXXXXX" required="">
            </div>
        </div>
    </form>

    <button @click="nextStep" class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
        Next Step: <b>Shipping Info</b>
    </button> 
   </div> 


    <!-- Step 2 -->
    <div v-if="index === 1">
    <form action="#" >
        <h3 class="mb-4 text-lg font-bold leading-none text-gray-900 dark:text-white">Shipping Info</h3>
        <div class="grid gap-4 mb-4 sm:grid-cols-2">
            <div>
  
                <label  class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"><b>Choose Shipping Style:</b></label>

                <ul class="w-auto text-sm font-medium text-gray-900 bg-white border border-gray-200 rounded-lg dark:bg-gray-700 dark:border-gray-600 dark:text-white">
                    <li class=" p-2 w-full border-b border-gray-200 rounded-t-lg dark:border-gray-600">
                        <div class="flex items-center pl-3">
                            <input v-model="ShippingType" id="list-radio-license" type="radio" value="" name="list-radio" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-700 dark:focus:ring-offset-gray-700 focus:ring-2 dark:bg-gray-600 dark:border-gray-500">
                            <div class="ml-2 text-sm">
                                <label for="helper-radio" class="font-medium text-gray-900 dark:text-gray-300">Express Shipping</label>
                                <p id="helper-radio-text" class="text-xs font-normal text-gray-500 dark:text-gray-300">Shorter Delivery time with extra charges</p>
                            </div>
                        </div>
                    </li>
                    <li class="p-2 w-full border-b border-gray-200 rounded-t-lg dark:border-gray-600">
                        <div class="flex items-center pl-3">
                            <input v-model="ShippingType" id="list-radio-license" type="radio" value="" name="list-radio" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-700 dark:focus:ring-offset-gray-700 focus:ring-2 dark:bg-gray-600 dark:border-gray-500">
                            <div class="ml-2 text-sm">
                                <label for="helper-radio" class="font-medium text-gray-900 ">Standard Shipping </label>
                                <p id="helper-radio-text" class="text-xs font-normal text-gray-500 ">No extra charge</p>
                            </div>
                        </div>
                    </li>
                </ul>
                
            </div>

            <div>
            <label  class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"><b>Items Available:</b></label>

            <ul class="grid w-full gap-6 md:grid-cols-3">
                <li v-for="item in items" :key="item.id">
                  <input
                    type="checkbox"
                    :id="item.id"
                    v-model="selectedItems"
                    :value="item"
                    class="hidden peer"
                  >
                  <label
                    :for="item.id"
                    class="inline-flex items-center justify-between w-full p-5 text-gray-500 bg-white border-2 border-gray-200 rounded-lg cursor-pointer dark:hover:text-gray-300 dark:border-gray-700 peer-checked:border-blue-600 hover:text-gray-600 dark:peer-checked:text-gray-300 peer-checked:text-gray-600 hover:bg-gray-50 dark:text-gray-400 dark:bg-gray-800 dark:hover:bg-gray-700"
                  >
                    <div class="block">
                      <div class="w-full text-lg font-semibold">{{ item.name }}</div>
                      <div class="w-full text-sm">{{ item.location }}</div>
                    </div>
                  </label>
                </li>
              </ul>
        </div>
        </div>
        
    </form>
    <button @click="previousStep" class="text-white mx-8 bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
        Back
    </button> 
    <button @click="nextStep" class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
        Next: <b>Payment Info</b>
    </button> 
    

</div>


    <!-- Step 3 -->
    <div v-if="index===2">

            <div class="credit-card w-full sm:w-auto shadow-lg mx-auto rounded-xl" v-show="card === 'front'">
                
                <div class="relative">
                  <img class="w-full h-auto" src="https://www.computop-paygate.com/Templates/imagesaboutYou_desktop/images/svg-cards/card-visa-front.png" alt="front credit card" />
                  <div class="front bg-transparent text-lg w-full text-white px-12 absolute left-0 bottom-12">
                    <p class="number mb-5 sm:text-xl" v-text="cardNumber !== '' ? cardNumber : '0000 0000 0000 0000'"></p>
                    <div class="flex flex-row justify-between">
                      <p v-text="cardholder !== '' ? cardholder : 'Card holder'"></p>
                      <div class="">
                        <span v-text="expired.month"></span>
                        <span v-show="expired.month !== ''">/</span>
                        <span v-text="expired.year"></span>
                      </div>
                    </div>
                  </div>
                </div>
                
                
                <h3 class="px-8 text-lg font-bold leading-none text-gray-900 dark:text-white">Card Payment</h3>

              <main class=" p-4">
                <div>
                  <div class="my-3">
                    <input
                      type="text"
                      class="block w-full px-5 py-2 border rounded-lg bg-white shadow-lg placeholder-gray-400 text-gray-700 focus:ring focus:outline-none"
                      placeholder="Card holder"
                      maxlength="22"
                      v-model="cardholder"
                      required=""
                    />
                  </div>
                  <div class="my-3">
                    <input
                      type="text"
                      class="block w-full px-5 py-2 border rounded-lg bg-white shadow-lg placeholder-gray-400 text-gray-700 focus:ring focus:outline-none"
                      placeholder="Card number"
                      v-model="cardNumber"
                      @keydown="format"
                      maxlength="19"
                      required=""
                    />
                  </div>
                  <div class="my-3 flex flex-col">
                    <div class="mb-2">
                      <label for="" class="text-gray-700">Expired Date</label>
                    </div>
                    <div class="grid grid-cols-2 sm:grid-cols-4 gap-2">
                      <select
                        name=""
                        id=""
                        class="form-select appearance-none block w-full px-5 py-2 border rounded-lg bg-white shadow-lg placeholder-gray-400 text-gray-700 focus:ring focus:outline-none"
                        v-model="expired.month"
                      >
                        <option value="" disabled selected>MM</option>
                        <option value="01">01-January</option>
                        <option value="02">02-February</option>
                        <option value="03">03-March</option>
                        <option value="04">04-April</option>
                        <option value="05">05-May</option>
                        <option value="06">06-June</option>
                        <option value="07">07-July</option>
                        <option value="08">08-August</option>
                        <option value="09">09-September</option>
                        <option value="10">10-October</option>
                        <option value="11">11-November</option>
                        <option value="12">12-December</option>
                      </select>
                      <select
                        name=""
                        id=""
                        class="form-select appearance-none block w-full px-5 py-2 border rounded-lg bg-white shadow-lg placeholder-gray-400 text-gray-700 focus:ring focus:outline-none"
                        v-model="expired.year"
                      >
                        <option value="" disabled selected>YY</option>
                        <option value="2021">2021</option>
                        <option value="2022">2022</option>
                        <option value="2023">2023</option>
                        <option value="2024">2024</option>
                        <option value="2025">2025</option>
                        <option value="2026">2026</option>
                      </select>
                      <input
                        type="tel"
                        class="block w-full col-span-2 px-5 py-2 border rounded-lg bg-white shadow-lg placeholder-gray-400 text-gray-700 focus:ring focus:outline-none"
                        placeholder="Security code"
                        maxlength="4"
                        v-model="securityCode"
                        required=""
                      />
                    </div>
                  </div>
                </div>
              </main>
              <footer >
                <button
                data-modal-target="popup-modal" data-modal-toggle="popup-modal" 
                  class="submit-button px-4 py-3 rounded-full bg-blue-300 text-blue-900 focus:ring focus:outline-none w-full text-xl font-semibold transition-colors">
                  Confirm
                </button>
                <button @click="previousStep"
                  class="submit-button mt-2 px-4 py-3 rounded-full bg-blue-300 text-blue-900 focus:ring focus:outline-none w-full text-xl font-semibold transition-colors">
                  Go Back
                </button>
                <div id="popup-modal" tabindex="-1" class="fixed top-0 left-0 right-0 z-50 hidden p-4 overflow-x-hidden overflow-y-auto md:inset-0 h-[calc(100%-1rem)] max-h-full">
                    <div class="relative w-full max-w-md max-h-full">
                        <div class="relative bg-white rounded-lg shadow dark:bg-gray-700">
                            <button type="button" class="absolute top-3 right-2.5 text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm p-1.5 ml-auto inline-flex items-center dark:hover:bg-gray-800 dark:hover:text-white" data-modal-hide="popup-modal">
                                <svg aria-hidden="true" class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
                                <span class="sr-only">Close modal</span>
                            </button>
                            <div class="p-6 text-center">
                                <svg aria-hidden="true" class="mx-auto mb-4 text-gray-400 w-14 h-14 dark:text-gray-200" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4m0 4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                                <h3 class="mb-5 text-lg font-normal text-gray-500 dark:text-gray-400">Shipping Confirmation</h3>
                                <p class=" text-lg font-normal text-gray-500"> Hello, {{ UserData.Name }} your item(s) : {{selectedNames}} is being shipped. </p>
                                <button data-modal-hide="popup-modal" type="button" class="text-white bg-red-600 hover:bg-red-800 focus:ring-4 focus:outline-none focus:ring-red-300 dark:focus:ring-red-800 font-medium rounded-lg text-sm inline-flex items-center px-5 py-2.5 text-center mr-2">
                                    Yes, I'm sure
                                </button>
                                <button data-modal-hide="popup-modal" type="button" class="text-gray-500 bg-white hover:bg-gray-100 focus:ring-4 focus:outline-none focus:ring-gray-200 rounded-lg border border-gray-200 text-sm font-medium px-5 py-2.5 hover:text-gray-900 focus:z-10 dark:bg-gray-700 dark:text-gray-300 dark:border-gray-500 dark:hover:text-white dark:hover:bg-gray-600 dark:focus:ring-gray-600">No, cancel</button>
                            </div>
                        </div>
                    </div>
                </div>
              </footer>
              
            </div>
            

    </div>
    <!-- <form action="#" v-if="index === 2">
        <h3 class="mb-4 text-lg font-bold leading-none text-gray-900 dark:text-white">Payment Info</h3>
        <div class="grid gap-4 mb-4 sm:grid-cols-2">
            <div>
                <label for="username" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Username</label>
                <input v-model="Username" type="text" name="username" id="username" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-600 focus:border-blue-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="username.example" required="">
            </div>
            <div>
                <label for="email" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Email</label>
                <input v-model="UserEmail" type="email" name="email" id="email" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-600 focus:border-blue-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="name@company.com" required="">
            </div>
            <div>
                <label for="gps" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">GPS Address</label>
                <input v-model="UserGPS" type="text" name="gps" id="gps" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-600 focus:border-blue-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="gps-address.example" required="">
            </div>
            <div>
                <label for="address2" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Postal Address </label>
                <input v-model="UserPAddress" type="text" name="address2" id="address2" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-600 focus:border-blue-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="postal-address.example" required="">
            </div>
            <div>
                <label for="phone" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Phone Number</label>
                <input v-model="UserPhone" type="tel" name="tel" id="tel" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-600 focus:border-blue-600 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="0XXXXXXXXX" required="">
            </div>
        </div>
        
    </form> -->

   



</div>
        
    
    </div>

</template>


<style scoped>
.form-select {
    background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' fill='none' viewBox='0 0 20 20'%3e%3cpath stroke='%239ca3af' stroke-linecap='round' stroke-linejoin='round' stroke-width='1.5' d='M6 8l4 4 4-4'/%3e%3c/svg%3e");
    background-repeat: no-repeat;
    background-position: right 0.5rem center;
    background-size: 1.5em 1.5em;
    -webkit-tap-highlight-color: transparent;
  }

 

  .credit-card {
    max-width: 420px;
  }

  @media only screen and (max-width: 420px) {
    .credit-card .front {
      font-size: 100%;
      padding: 0 2rem;
      bottom: 2rem !important;
    }

    .credit-card .front .number {
      margin-bottom: 0.5rem !important;
    }
  }


</style>