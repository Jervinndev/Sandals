<script setup>
import { ref } from 'vue';
import { Scaling, CircleCheckBig, Van, Star, ChevronRight, ChevronLeft } from 'lucide-vue-next';

const feature = ref([
    { id: 1, icon: Scaling, title: 'Size Guide', info: 'Perfect fit, every time. See our sizing guide to choose the right pair for you.' },
    { id: 2, icon: CircleCheckBig, title: 'Guest Checkout', info: 'Shop faster. Checkout as a guest and get your favorites delivered to your door in no time.' },
    { id: 3, icon: Van, title: 'Order Tracking', info: 'Track your package in seconds. Get instant updates on your order’s journey.' }
])
</script>

<template>
    <section class="p-5 sm:py-15 py-6">
        <main class="grid gap-4 mx-auto max-w-7xl w-full">
            <div class="font-Poppins">
                <h1 class="text-2xl font-bold font-outfit text-orange-950">Features</h1>
                <p class="text-orange-950 font-outfit">Perfectly designed for both professional workdays and special
                    events.</p>
            </div>
            <div class="grid 2xl:grid-cols-3 md:grid-cols-3 grid-cols-1 gap-3.5 font-Poppins">
                <div v-for="feat in feature" :key="feat.id"
                    class="flex flex-col gap-2 border border-black/10 p-5 rounded-2xl bg-white">
                    <component :is="feat.icon" color="orange" />
                    <h1 class="font-bold text-black/80">{{ feat.title }}</h1>
                    <p class="text-orange-950 font-outfit">{{ feat.info }}</p>
                </div>
            </div>
        </main>
    </section>
</template>