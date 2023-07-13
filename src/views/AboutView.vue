<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';
import LocomotiveScroll from 'locomotive-scroll';


const scrollRef = ref(null);

onMounted(() => {
  scrollRef.value = new LocomotiveScroll({
    el: document.querySelector("#scroll-container")
  });
});

onBeforeUnmount(() => {
  scrollRef.value.destroy();
});


</script>
<template>
  <section id="scroll-container" class="px-2 sm:px-10 lg:px-20 bg-gradient-to-r from-amber-100 to-teal-50">
    <section class="mb-4 flex flex-col md:flex-row gap-y-4 md:space-x-4  rounded-md p-6">
      <section class="w-full md:w-full p-4 text-center">
        <div class="text-center md:text-left">
          <!-- <h1 class="text-3xl font-semibold">
            Hello I'm
            <span class="text-clip from-amber-500 to-teal-500">
              Emmanuel
            </span>
          </h1> -->
          <h1 class="font-sans text-3xl md:text-4xl font-semibold text-zinc-800">Hy! I Am<br>
            <span class="text-clipper from-amber-500 from-50% via-pink-500 to-yellow-300">Emmanuel
              Facardos</span>
          </h1>
          <div class="text-2xl text-gray-600 md:w-64 mt">
            <br>
            <span class="text-clip from-amber-500 to-teal-400">
              Web Developer, Graphics Designer, & UI/UX Designer</span>
          </div>
        </div>

        <div class=" mt-10">
          <button class="btn-default-2">
            Hire me
          </button>
        </div>

        <div class="relative w-full">
          <div class="w-20 h-20 rounded-full absolute bg-gradient-to-l from-teal-200/50 to-amber-200/25 top-0"></div>
          <div
            class="w-28 h-28 rounded-full absolute bg-gradient-to-l from-teal-100 to-amber-200/50 bottom-0 md:bottom-5 right-10">
          </div>
          <div class="w-10 h-10 rounded-full absolute bg-gradient-to-l from-teal-100 to-amber-200/50 right-0">
          </div>
          <div class="w-4 h-4 rounded-full absolute bg-gradient-to-l from-teal-100 to-amber-200/50 right-5">
          </div>
        </div>

        <!-- HERE -->
      </section>
      <section class="w-full md:w-full relative">
        <div
          class="rounded-[100px] overflow-hidden flex justify-center items-center shadow-lg shadow-teal-500/50 backdrop-blur-sm">
          <img src="../assets/images/emma_img.jpeg" class="me-image w-inherit" />
        </div>

      </section>
    </section>


    <section class="flex flex-col md:flex-row gap-y-4 md:space-x-4 rounded-md p-6">
      <section class="w-full md:w-full p-4">
        <div class="relative w-full">
          <div class="w-20 h-20 rounded-full absolute bg-gradient-to-l from-teal-200/50 to-amber-200/25 top-0"></div>
          <div class="w-28 h-28 rounded-full absolute bg-gradient-to-l from-teal-100 to-amber-200/50 bottom-0 right-10">
          </div>
        </div>

        <h1 class="text-3xl font-semibold about-h1 text-clip from-teal-500 via-pink-500">About me</h1>
      </section>
      <section class="w-full md:w-full p-6 ">
        <div class="relative w-full">
          <div class="w-20 h-20 rounded-full absolute bg-gradient-to-l from-teal-100 to-amber-200/50 left-0 bottom-20">
          </div>
          <div class="w-10 h-10 rounded-full absolute bg-gradient-to-l from-teal-100 to-amber-200/50 bottom-0 right-10">
          </div>
        </div>
        <p class="font-semibold text-clip from-teal-500 via-pink-500 to-amber-500 leading">

          I'm passionate about
          <span class="text-xl">
            Graphics Design, Web Development, UI/UX, Mobile Development, Desktop Apps. &nbsp;
          </span>
          I believe
          that life is a continuous journey of learning and growth, and I'm constantly seeking new experiences and
          opportunities to expand my horizons.

          With a background and experience in <span class="text-xl text-clip from-blue-500 to-blue-600">ReactJs</span>,
          <span class="text-xl text-clip from-green-500 to-teal-600">VueJS</span>, <span
            class="text-xl text-clip from-indigo-600 to-blue-600">TailwindCss</span> and
          <span class="text-xl text-clip from-fuchsia-600 to-red-500">Php Laravel</span>.
        </p>
      </section>
    </section>
  </section>
</template>
