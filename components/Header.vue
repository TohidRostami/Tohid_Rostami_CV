<template>
    <header class="fixed top-0 left-0 right-0 h-16 bg-white z-[1000] flex items-center justify-end px-4">
        <!-- Burger icon -->
        <button @click="toggleMenu" class="z-[1100] bg-transparent border-none cursor-pointer">
            <svg class="w-6 h-6 stroke-[2] stroke-gray-800" viewBox="0 0 24 24" fill="none"
                 stroke="currentColor" stroke-linecap="round" stroke-linejoin="round">
                <path d="M4 6h16M4 12h16M4 18h16" />
            </svg>
        </button>

        <!-- Slide-in Menu -->
        <div :class="[
      'fixed top-0 right-0 h-16 overflow-hidden bg-white transition-all duration-500 ease-in-out flex items-center justify-center z-[1050]',
      menuOpen ? 'w-full' : 'w-0'
    ]">
            <nav class="w-2/5 flex items-center justify-between px-4">
                <a href="/" class="text-gray-800 font-medium hover:text-blue-500">Home</a>
                <a href="/about" class="text-gray-800 font-medium hover:text-blue-500">About</a>
                <a href="/contact" class="text-gray-800 font-medium hover:text-blue-500">Contact</a>
            </nav>
        </div>
    </header>
</template>

<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)
function toggleMenu() {
    menuOpen.value = !menuOpen.value
}
</script>
