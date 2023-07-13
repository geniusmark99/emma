<script setup>
import TextLoader from '../components/TextLoader.vue';
</script>

<template>
    <!-- Home Top -->
    <div class="flex flex-col-reverse md:flex-row md:justify-between gap-y-5 md:gap-x-20 default-pd">
        <div class="w-full">
            <p>
            <h1 class="font-sans text-3xl md:text-4xl font-semibold text-zinc-800">Hy! I Am<br>
                <span class="text-clipper from-amber-500 from-50% via-pink-500 to-yellow-300">Emmanuel
                    Facardos</span>
            </h1>
            </p>
            <p class="mt-8 font-normal text-gray-800 text-md leading-7">
                Hello and welcome to my Portfolio page! I'm a dynamic and creative software developer with a passion for
                <span class="text-clipper from-yellow-200 to-amber-600 font-semibold">Web Development technologies i.e:

                </span>&nbsp;
                <span class="text-clipper from-yellow-200 to-amber-600 font-semibold"> Laravel,Php,Java,React,Vue,tailwind
                </span>
            </p>

            <button class="btn-default mt-8">
                Hire me
            </button>
        </div>
        <div class="w-full">
            <img src="../assets/images/ui-bg.jpg" class="rounded-lg" />
        </div>
    </div>
    <!--End Home Top -->

    <!-- Home Bottom -->
    <div class="grid grid-cols-1 md:grid-cols-2 default-pd mt-10 md:mt-20">
        <div class="flex flex-col w-full py-12 px-4">
            <p class="text-zinc-900 text-2xl md:text-3xl font-semibold">
                My awesome <br>
                <span class="text-amber-500">services</span>
            </p>
            <div>
                <p
                    class="mt-6 w-full md:w-48  shadow-lg shadow-amber-100 p-4 rounded-md text-clipper from-fuchsia-500 to-amber-500">
                    My services are the ultimate solution to your business and brand, delivering unparalleled platform that
                    will exceed your expectations.
                </p>
                <button class="btn-default mt-8">Downnload My CV</button>
            </div>
        </div>

        <div class="shadow-lg shadow-amber-100 p-4 rounded-md flex flex-col items-center gap-y-10" id="mobile_design">
            <!-- <div class="card-icon">

            </div> -->
            <h2 class="card-title font-bold font-mono text-3xl text-clipper from-fuchsia-500 to-amber-500">Design</h2>
            <p class="card-content leading-6 bg-clip-text text-transparent bg-gradient-to-tl from-fuchsia-500 to-amber-500">
                My design skills are simply incredible, with a keen eye for detail and a knack for creating beautiful,
                visually stunning works of art. I have an amazing ability to conceptualize and execute creative design
                ideas, always pushing the boundaries and delivering exceptional results.
            </p>
            <div class="flex justify-center items-center">
                <!-- x -->
            </div>
        </div>


    </div>
    <TextLoader />

    <!-- End Home Bottom -->
</template>
<style scoped>
#mobile_design {
    position: relative;
}

#mobile_design:after {
    position: absolute;
    content: "";
    top: 0;
    background-image: url('../assets/images/mobile-design.svg');
    background-repeat: no-repeat;
    background-size: cover;
}
</style>