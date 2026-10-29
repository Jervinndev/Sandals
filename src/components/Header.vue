<script setup>
import { ShoppingCart, User, Heart, ChevronDown, Footprints } from 'lucide-vue-next';
</script>

<template>
    <header class="w-full flex items-center justify-center p-5 font-Poppins fixed z-10 ">
        <div
            class="mx-auto max-w-7xl w-full bg-white text-black border border-black/10 flex items-center justify-between shadow-lg shadow-gray-200/5 p-4 rounded-xl">
            <div class="flex item-center gap-2.5 font-black text-orange-400">
                <img src="/src/assets/high-heel-svgrepo-com (1).svg" alt="" class="h-5 text-orange-400">
                <h1><span class="font-outfit">Solei & Co</span></h1>
            </div>
            <nav class="2xl:flex hidden items-center justify-center">
                <ul class="flex items-center justify-center gap-4 text-sm text-orange-950">
                    <li>Shop All</li>
                    <div class="flex items-center justify-center gap-1">
                        <li>Categories</li>
                        <ChevronDown size="20" />
                    </div>
                    <li>New Arrivals</li>
                    <li>Sale/Promos</li>
                </ul>
            </nav>
            <div class="flex items-center justify-center gap-4 text-sm">
                <ShoppingCart color="#5B5B5B" />
                <User color="#5B5B5B" />
                <router-link to="/Register"
                    class="bg-orange-400 text-white p-2 rounded-xl w-27 hover:bg-orange-400/90 font-outfit 2xl:flex hidden items-center justify-center">Get
                    started</router-link>
            </div>
        </div>
    </header>
</template>