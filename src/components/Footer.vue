<script setup>
import { RouterLink } from 'vue-router';
import EmailIcon from './icons/EmailIcon.vue';
import WhatsappIcon from './icons/WhatsappIcon.vue';
import Linkedin from './icons/Linkedin.vue';


</script>
<template>
    <footer
        class="py-10 px-2 pt-2 sm:px-10 lg:px-20 bg-gradient-to-tl from-amber-400 from-5% text-white to-amber-600 w-full h-auto bottom-0">
        <div class="flex flex-col md:flex-row gap-y-10 md:gap-y-2 md:justify-between">
            <div class="text-center">
                <p class="font-semibold text-2xl">
                    I Listen<br>
                    You Prosper
                </p>
            </div>
            <div class="text-center">

                <h2 class="font-semibold text-2xl mb-4 md:text-left uppercase font-sans">Site</h2>
                <ul class="flex flex-col gap-y-4 md:text-left">
                    <li>
                        <RouterLink to="/about">
                            About me
                        </RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/contact">
                            Contact me
                        </RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/">
                            Home
                        </RouterLink>
                    </li>
                </ul>
            </div>
            <div class="text-center">
                <h2 class="font-semibold text-2xl mb-4 md:text-left uppercase font-sans">Contact</h2>
                <ul class="flex flex-col gap-y-4 items-center md:items-start md:text-left">

                    <li class="text-justify">
                        <a href="mailto:markthavalor@gmail.com" class="underline flex gap-x-4 items-center">
                            <div class="contact_icon">
                                <EmailIcon />
                            </div>
                            <span>
                                Email me
                            </span>

                        </a>
                    </li>

                    <li class="text-justify">
                        <a href="https://wa.me/2348141625004" class="underline flex gap-x-4" target="_blank">
                            <div class="contact_icon">
                                <WhatsappIcon />
                            </div>

                            <span>
                                Whatsapp me
                            </span>

                        </a>
                    </li>
                    <!-- <li class="text-justify">
                        <a href="https://wa.me/2347056951660" class="underline flex gap-x-4">
                            <div class="contact_icon">
                                <Linkedin />
                            </div>

                            <span>
                                Linkedin
                            </span>
                        </a>
                    </li> -->
                </ul>
            </div>
        </div>
        <div class="fixed bottom-0 font- font-sans thin text-sm">

        </div>
    </footer>
</template>

<style scoped>
.contact_icon svg {
    width: 20px;
    height: 20px;
}
</style>
