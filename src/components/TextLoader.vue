<template>
    <div class="text-center bottom-0 relative mt-20">
        <div class="loader">
            <span class="bg-amber-300"></span>
            <span class="bg-amber-400"></span>
            <span class="bg-amber-500"></span>
        </div>
    </div>
</template>
<style scoped>
.loader {
    display: inline-block;
    position: relative;
    width: 64px;
    height: 64px;
}

.loader span {
    position: absolute;
    top: 0;
    left: 0;
    width: 12px;
    height: 12px;
    border-radius: 50%;
    /* background: #000; */
    animation: loader-animation 1.2s cubic-bezier(0, 0.5, 0.5, 1) infinite;
}

.loader span:nth-child(2) {
    transform: translateX(20px);
}

.loader span:nth-child(3) {
    transform: translateX(40px);
}

@keyframes loader-animation {
    0% {
        transform: scale(0);
        opacity: 1;
    }

    100% {
        transform: scale(1);
        opacity: 0;
    }
}
</style>
