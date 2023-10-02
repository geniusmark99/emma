<script setup>
import '../assets/styles/links.css';
import { onMounted } from 'vue';
import { RouterLink } from 'vue-router';
import Hamburger from './icons/Hamburger.vue';
import HomeIcon from './icons/HomeIcon.vue';
import AboutIcon from './icons/AboutIcon.vue';
import ServicesIcon from './icons/ServicesIcon.vue';
import CloseIcon from './icons/CloseIcon.vue';
import Loader from './Loader.vue';


function OpenMobileBar() {
    const MobileSide = document.getElementById("mobile-sidebar");
    MobileSide.classList.add("show");
}

function CloseMobileBar() {
    const MobileSide = document.getElementById("mobile-sidebar");
    MobileSide.classList.remove("show");
}

onMounted(() => {
    document.addEventListener('keydown', function (event) {
        const MobileSide = document.getElementById("mobile-sidebar");
        if (event.key === "Escape") {
            event.preventDefault();
            if (MobileSide.classList.contains("show")) {
                MobileSide.classList.remove("show");
            } else {
                return false;
            }

        }
    });
});


</script>

<template>
    <header class="h-16 bg-white">
        <nav class="px-2 pt-2 sm:px-10 lg:px-20 flex justify-between items-center">
            <div>
                <div class="md:hidden w-6 h-6 hover:cursor-pointer" @click="OpenMobileBar">
                    <Hamburger />
                </div>

                <div id="mobile-sidebar">
                    <button @click="CloseMobileBar" title="Esc to Close">
                        <span>
                            Close
                        </span>
                        <CloseIcon />
                    </button>
                    <div id="mobile-sidebar-content">
                        <ul class="flex gap-10 md:gap-14 text-xs sm:text-lg">
                            <li class="font-semibold">
                                <RouterLink to="/" class="links_mob">
                                    <HomeIcon />
                                    <span>
                                        Home
                                    </span>
                                </RouterLink>
                            </li>
                            <li class="font-semibold">
                                <RouterLink to="/about" class="links_mob">
                                    <AboutIcon />
                                    <span class="whitespace-nowrap">
                                        About us
                                    </span>
                                </RouterLink>
                            </li>
                            <li class="font-semibold">
                                <RouterLink to="/services" class="links_mob">
                                    <ServicesIcon />
                                    <span>
                                        Services
                                    </span>
                                </RouterLink>
                            </li>
                        </ul>

                    </div>
                </div>


                <div
                    class="whitespace-nowrap font-mono hidden md:flex items-center bg-clip-text text-2xl font-bold text-transparent bg-gradient-to-br from-amber-400 to-amber-500  md:w-48 text-center">
                    <span
                        class="font-sans font-semibold text-clipper  text-3xl md:text-4xl from-amber-500 from-50% via-pink-500 to-yellow-300">Emmanuel
                    </span>
                    <Loader />

                </div>
            </div>
            <div
                class="whitespace-nowrap flex font-mono md:hidden bg-clip-text text-2xl font-bold text-transparent bg-gradient-to-br from-amber-400 to-amber-500 md:w-40 text-center">
                <span
                    class="font-sans font-semibold text-clipper text-2xl from-amber-500 from-50% via-pink-500 to-yellow-300">Emmanuel
                </span>

                <Loader />
            </div>
            <div class=" text-stone-950 flex w-auto gap-20 items-center">
                <ul class="hidden md:flex justify-between gap-20 w-full font-semibold">
                    <li>
                        <RouterLink to="/" class="links">
                            <HomeIcon />
                            Home
                        </RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/about" class="links">
                            <AboutIcon />
                            About Me
                        </RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/services" class="links">
                            <ServicesIcon />
                            Services
                        </RouterLink>
                    </li>
                </ul>

                <a href="https://wa.me/2348141625004" target="_blank" class="btn-default"> Contact me </a>
            </div>
        </nav>
    </header>
</template>
