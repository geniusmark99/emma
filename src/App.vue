<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import WhatsappIcon from './components/icons/WhatsappIcon.vue';
</script>

<template>
  <Header />
  <main class="mt-8 h-auto mb-20 pb-20">
    <RouterView />
  </main>
  <div title="Click let build your project" id="whatapp-floating-btn"
    class="shadow-lg hover:shadow-amber-400 fixed w-16 h-16 bg-amber-500 bottom-10 right-10 rounded-full p-4 flex items-center justify-center">
    <a class="w-13 h-13 flex justify-center items-center" href="https://wa.me/2347056951660" target="_blank">
      <WhatsappIcon class="w-8" />
    </a>
  </div>
  <Footer />
</template>

<style scoped>
#whatapp-floating-btn:hover:before {
  background-image: linear-gradient(to right, rgb(20 184 166), rgb(34 211 238));
}

#whatapp-floating-btn {
  animation: bounce 2s infinite;
}

#whatapp-floating-btn:before {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background-color: rgba(255, 193, 7, 0.7);
  transform: scale(0);
  opacity: 0;
  border-radius: 50%;
  animation: ripple 1s infinite;
}

@keyframes bounce {
  0% {
    transform: translateY(0);
  }

  50% {
    transform: translateY(-10px);
  }

  75% {
    transform: translateY(0);
  }

  100% {
    transform: translateY(-5px);
  }
}




@keyframes ripple {
  0% {
    transform: scale(0);
    opacity: 0.5;
  }

  50% {
    opacity: 0.2;
  }



  100% {
    transform: scale(2);
    opacity: 0;
  }
}
</style>
