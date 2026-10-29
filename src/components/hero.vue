<script setup>
import { ref } from 'vue';
import { Scaling, CircleCheckBig, Van, Star, ChevronRight, ChevronLeft } from 'lucide-vue-next';

const imgs = ref([
    { id: 1, img: '/src/assets/download (8)(1).jpg' },
    { id: 2, img: '/src/assets/download (9).jpg' },
    { id: 3, img: '/src/assets/download (10).jpg' },
    { id: 4, img: '/src/assets/download (11).jpg' },
])
</script>
<template>
    <section class="p-5 pt-23">
        <main class="grid 2xl:grid-cols-2 md:grid-cols-2 grid-cols-1 place-content-center mx-auto max-w-7xl w-full">
            <div class="flex flex-col items-start justify-center gap-4 w-fit pt-8 2xl:pt-0">
                <h1 class="font-black 2xl:text-6xl text-3xl 2xl:w-150 w-full font-outfit text-orange-950">
                    BROWSE ALL
                    <span class="text-orange-400 ">AVAILABLE </span>STYLES
                </h1>
                <p class="text-lg font-outfit text-orange-950">Discover our collection of shoes, perfectly crafted for
                    every occasion from the
                    office
                    to an evening
                    out. Stylish, comfortable, and affordable.</p>
                <div class="flex gap-2.5 w-full font-outfit 2xl:flex-row md:flex-row">
                    <button class="bg-orange-400 p-2 2xl:w-40 w-full rounded-lg text-white
                    ">Shop now</button>
                    <button class="p-2 2xl:w-40 w-full border border-black/10 rounded-lg bg-white text-orange-950">Get
                        started</button>
                </div>
                <div class="border border-black/10 p-4 rounded-lg bg-white 2xl:w-fit w-full">
                    <div class="flex items-center justify-between gap-2 mb-3">
                        <div v-for="imges in imgs" :key="imges.id">
                            <img :src="imges.img" alt="" class="w-10 h-10 rounded-4xl">
                        </div>
                        <div
                            class="flex items-center justify-center text-white rounded-2xl bg-[#ff9c3a] w-20 border border-orange-200 ">
                            <span>Views</span>
                        </div>
                    </div>
                    <div class="flex items-center justify-between gap-3">
                        <p class="text-sm text-orange-950">Goods and high quality</p>
                        <div class="flex gap-1">
                            <Star v-for="n in 4" :key="n" color="orange" />
                        </div>
                    </div>
                </div>
            </div>
            <div class="relative w-fit flex items-center justify-center">
                <img src="/src/assets/Women Milley Pump -Beige.png" alt="" class="2xl:h-140">
                <div
                    class=" absolute flex items-center gap-3 right-0 p-2 rounded-lg 2xl:bottom-15 bottom-0 bg-white border border-black/10">
                    <img class="h-20" src="/src/assets/Women Milley Pump -Beige.png" alt="">
                    <div class="grid font-outfit text-sm gap-0.5 text-orange-950">
                        <h1 class="font-bold">Classic Pumps</h1>
                        <p>Stylish for both work and occasions.</p>
                        <button class="w-20 mt-1 p-1 bg-orange-400 text-white rounded-2xl">View all</button>
                    </div>
                </div>
                <div class="absolute flex items-center justify-between w-full">
                    <ChevronLeft />
                    <ChevronRight />
                </div>
            </div>
        </main>
    </section>
</template>