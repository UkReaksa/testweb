<template>
  <div class=" h-[100px] w-screen bg-slate-400 my-[-30px]"> 
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"
    />
    <!-- header -->

    <div class="flex justify-around my-[20px]">
     <!-- menu bar -->
      <div class=" absolute mr-[-350px] my-10" >
        <i @click="shownubar" class="fa-solid fa-bars cursor-pointer text-2xl sm:opacity-0"></i>
      </div>
      <!--  -->
      <ul v-if="show"
        class="mx-[200px] space-y-5 cursor-pointer bg-slate-500 absolute h-[360px] w-[700px] text-center px-[300px] text-white font-semibold py-5 my-[-20px]
        sm:flex gap-10 mr-[200px] sm:bg-inherit"
        
      >
        <!-- close button -->
      <div class=" px-[210px] py-5 absolute ">
        <i @click="shownubar" class="fa-solid fa-xmark text-2xl absolute hover:text-red-500 sm:opacity-0"></i>
      </div>
      <!--  -->
        <li class=" hover:bg-black w-[90px] h-[40px] rounded-lg p-2 sm:w-[120px]">
          ទំព័រដើម
        </li>
        <li class="hover:bg-black w-[90px] h-[40px] rounded-lg p-2">
          ជ្រើសរើស
        </li>
        <li class="hover:bg-black w-[90px] h-[40px] rounded-lg p-2">បង្ហាញ</li>
        <li class="hover:bg-black w-[90px] h-[40px] rounded-lg p-2">អំពី</li>
        <button
          class="w-[90px] h-[40px] bg-black rounded-lg hover:bg-slate-800"
        >
          ​Login
        </button>
      </ul>
     
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
export default {
  setup() {
    const show = ref(false);
    const shownubar = () => {
    show.value = !show.value;
   }
    return {
      show,
      shownubar,
    };
  },
};
</script>

