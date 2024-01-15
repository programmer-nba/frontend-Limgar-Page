
<template>
  <main>
    <section class="bg-[#064635] ">
      <nav class="container  mx-auto p-6 lg:flex lg:items-center lg:justify-between">
        <div class="flex items-center justify-between">
          <div>
            <button class="text-2xl font-bold text-[#F7FD04] neon lg:text-3xl">LIMGAR</button>
          </div>

          <!-- Mobile menu button -->
          <div class="flex lg:hidden">
            <button @click="isOpen = !isOpen" type="button"
              class="text-[#A6FF96]  focus:text-[#A6FF96] focus:outline-none " aria-label="toggle menu">
              <svg v-show="!isOpen" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
                stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M4 8h16M4 16h16" />
              </svg>

              <svg v-show="isOpen" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
                stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
              </svg>
            </button>
          </div>
        </div>

        <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
        <div :class="[isOpen ? 'translate-x-0 opacity-100 ' : 'opacity-0 -translate-x-full']"
          class="absolute inset-x-0 z-20 w-full  bg-white px-6 py-4 shadow-md transition-all duration-300 ease-in-out  lg:relative lg:top-0
           lg:mt-0 lg:flex lg:w-auto lg:translate-x-0 lg:items-center lg:bg-transparent lg:p-0 lg:opacity-100 lg:shadow-none lg:dark:bg-transparent">
          <div class="lg:-px-8 flex flex-col space-y-4 lg:mt-0 lg:flex-row lg:space-y-0">
            <button :class="{ 'text-[#004225] hover:text-[#1C7947]': isMobile, 'text-white hover:text-[#FFF47D]': !isMobile }"
              class="transform transition-colors duration-300  lg:mx-8">หน้าหลัก</button>
            <button :class="{ 'text-[#004225] hover:text-[#1C7947]': isMobile, 'text-white hover:text-[#FFF47D]': !isMobile }"
              class="transform transition-colors duration-300  lg:mx-8">สินค้า</button>
            <button onclick="window.open('http://limgar.nbadigital.tech/login', '_blank');"
              :class="{ 'bg-[#004225] text-[#fff]': isMobile, 'bg-[#F7FD04] text-[#064635]': !isMobile }"
              class="mt-4 block rounded-lg  px-6 py-2.5 text-center font-medium capitalize leading-5  hover:bg-[#FFD31D] lg:mt-0 lg:w-auto">
              เข้าสู่ระบบ</button>
          </div>


        </div>

      </nav>

      <div class="container mx-auto px-6 py-16 text-center">
        <div class="mx-auto max-w-lg">
          <h1 class="text-3xl font-bold text-white lg:text-4xl">LIMGAR
          </h1>
          <p class="mt-6 text-white ">จำหน่ายน้ำกระท่อม</p>
          <button onclick="window.open('http://limgar.nbadigital.tech/login', '_blank');"
            class="mt-6 rounded-lg bg-[#F7FD04] px-6 py-2.5 text-center text-sm font-medium capitalize leading-5 text-[#1F441E] hover:bg-[#FFD800] focus:outline-none lg:mx-0 lg:w-auto">
            เริ่มต้นใช้งาน</button>
        </div>

        <div class="flex justify-center mt-10 ">
          <swiper :centeredSlides="true" :autoplay="{
            delay: 3500,
            disableOnInteraction: false,
          }" :pagination="{ clickable: true, }" :modules="modules" class="flex justify-center">
            <swiper-slide>
              <img class=" w-full rounded-xl object-contain sm:object-contain lg:w-4/5" src="../assets/pr1.jpg" />
            </swiper-slide>
            <swiper-slide>
              <img class=" w-full rounded-xl object-contain sm:object-contain lg:w-4/5" src="../assets/pr2.jpg" />
            </swiper-slide>
            <swiper-slide>
              <img class=" w-full rounded-xl object-contain sm:object-contain lg:w-4/5" src="../assets/pr3.jpg" />
            </swiper-slide>
          </swiper>
        </div>

      </div>
    </section>



    <section class="bg-white ">
      <div class="h-[32rem] bg-[#BBDFC8] ">
        <div class="container mx-auto px-6 py-10">
          <h1 class="text-center text-3xl font-semibold capitalize text-[#064635] lg:text-4xl">สินค้าของเรา
          </h1>

          <div class="mx-auto mt-6 flex justify-center">
            <span class="inline-block h-1 w-40 rounded-full bg-[#1A4D2E]"></span>
            <span class="mx-1 inline-block h-1 w-3 rounded-full bg-[#1A4D2E]"></span>
            <span class="inline-block h-1 w-1 rounded-full bg-[#1A4D2E]"></span>
          </div>

          <!-- <p class="mx-auto mt-6 max-w-2xl text-center text-gray-500 dark:text-gray-300">Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo incidunt ex placeat modi magni quia error alias, adipisci rem similique, at omnis eligendi optio eos harum.</p> -->
        </div>
      </div>



      <div class="container mx-auto -mt-96 px-6 sm:-mt-96 md:-mt-96 relative ">
        <div class="mt-8 relative py-4">
          <swiper :pagination="{ dynamicBullets: true }" :slidesPerView="3" class="mySwiper ">
            <swiper-slide>
              <div class="flex flex-row mx-2 items-center rounded-xl border p-0 border-[#1A4D2E]  sm:p-6">
                <img class="aspect-square w-full rounded-xl object-cover" src="../assets/pr1.jpg" />
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex flex-row  mx-2 items-center rounded-xl border p-0 border-[#1A4D2E] sm:p-6">
                <img class="aspect-square w-full rounded-xl object-cover" src="../assets/pr2.jpg" alt="" />
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex flex-row  mx-2 items-center rounded-xl border p-0 border-[#1A4D2E] sm:p-6">
                <img class="aspect-square w-full rounded-xl object-cover" src="../assets/pr3.jpg" alt="" />
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex flex-row mx-2 items-center rounded-xl border p-0 border-[#1A4D2E] sm:p-6">
                <img class="aspect-square w-full rounded-xl object-cover" src="../assets/pr3.jpg" alt="" />
              </div>
            </swiper-slide>
            <swiper-slide>
              <div class="flex flex-row mx-2 items-center rounded-xl border p-0 border-[#1A4D2E] sm:p-6">
                <img class="aspect-square w-full rounded-xl object-cover" src="../assets/pr3.jpg" alt="" />
              </div>
            </swiper-slide>
          </swiper>

        </div>
      </div>



    </section>



    <footer class="bg-[#064635] ">
      <div class="container mx-auto px-6 py-12">
        <div class="md:-mx-3 md:flex md:items-center md:justify-between">
          <h1 class="text-3xl font-semibold tracking-tight text-white md:mx-3 xl:text-4xl">Subscribe
            our newsletter to get update.</h1>

          <div class="mt-6 shrink-0 md:mx-3 md:mt-0 md:w-auto">
            <button onclick="window.open('http://limgar.nbadigital.tech/login', '_blank');"
             class="inline-flex w-full items-center justify-center rounded-lg bg-[#9ADE7B] px-4 py-2 text-sm text-[#004225] duration-300 
              hover:bg-[#A6FF96] focus:ring focus:ring-gray-300 focus:ring-opacity-80">
              <span class="mx-2">เข้าสู่ระบบตอนนี้</span>

              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                stroke="currentColor" class="mx-2 h-6 w-6">
                <path stroke-linecap="round" stroke-linejoin="round" d="M17.25 8.25L21 12m0 0l-3.75 3.75M21 12H3" />
              </svg>
            </button>
          </div>
        </div>

        <hr class="my-6 border-gray-200 dark:border-gray-700 md:my-10" />

        <div class="grid grid-cols-1 gap-6 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">






          <div>
            <p class="font-semibold text-white">ติดต่อเรา</p>

            <div class="mt-5 flex flex-col items-start space-y-2">
              <a href="#"
                class=" transition-colors duration-300 hover:text-blue-500 hover:underline text-gray-300 dark:hover:text-blue-400">+880
                768 473 4978</a>
              <a href="#"
                class="transition-colors duration-300 hover:text-blue-500 hover:underline text-gray-300 dark:hover:text-blue-400">limgar@gmail.com</a>
            </div>
          </div>
        </div>

        <hr class="my-6 border-gray-200 dark:border-gray-700 md:my-10" />

        <div class="flex flex-col items-center justify-between sm:flex-row">
          <a href="#"
            class="text-2xl font-bold  transition-colors duration-300 hover:text-[#FBFF00] text-white dark:hover:text-gray-300">LIMGAR</a>

          <p class="mt-4 text-sm text-gray-300 sm:mt-0">© Copyright 2024. All Rights Reserved.</p>
        </div>
      </div>
    </footer>
  </main>
</template>


<script>
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import { Autoplay, Navigation, Pagination } from 'swiper/modules';
import { Swiper, SwiperSlide } from 'swiper/vue';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      isOpen: false,
      isMobile: false,
    };
  },
  mounted() {
    this.isMobile = window.innerWidth < 768;
    window.addEventListener('resize', this.handleResize);
  },
  beforeDestroy() {
    window.removeEventListener('resize', this.handleResize);
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
    },
    handleResize() {
      this.isMobile = window.innerWidth < 768;
    },
  },
  setup() {
    return {
      modules: [Autoplay, Pagination, Navigation],
    };
  },
};
</script>

<style scoped>
@import 'tailwindcss/base';
@import 'tailwindcss/components';
@import 'tailwindcss/utilities';

.swiper-slide {
  text-align: center;
  font-size: 18px;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
}

.neon:hover {
  color: #FFE300;

}
</style>
