<script setup>
import { ref } from 'vue';
import { Scaling, CircleCheckBig, Van, Star, ChevronRight, ChevronLeft } from 'lucide-vue-next';

import img1 from '../assets/pangalawa.jpg'
import img2 from '../assets/pangatlo.jpg'
import img3 from '../assets/pangapat.jpg'
import img4 from '../assets/Women Milley Pump -Beige.png'

const categories = ref([
    { id: 1, catimg: img1 },
    { id: 2, catimg: img2 },
    { id: 3, catimg: img3},
    { id: 4, catimg: img4 }
])
</script>

<template>
    <section class="pt-12 p-5">
        <div class="grid gap-4 mx-auto max-w-7xl w-full">
            <div class="flex justify-between">
                <div class="font-Poppins">
                    <h1 class="text-2xl font-bold font-outfit text-orange-950">Shop with categories</h1>
                    <p class="text-orange-950">Pang-opisina at pang-okasyon</p>
                </div>
                <div class="flex gap-2">
                    <div class="p-2 bg-orange-400 rounded-3xl text-white h-fit">
                        <ChevronLeft />
                    </div>
                    <div class="p-2 rounded-3xl border border-black/10 h-fit">
                        <ChevronRight />
                    </div>
                </div>
            </div>
            <div class="flex gap-2">
                <div v-for="cats in categories" :key="cats.id" class="flex relative overflow-auto">
                    <img :src="cats.catimg" alt="" class="rounded-2xl">
                    <div
                        class="absolute 2xl:bottom-12 bottom-1 2xl:right-4 right-1 p-2 border border-black/10 rounded-3xl">
                        <ChevronRight />
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>