<template>
  <nav class="container bg-white border-b border-gray-200 shadow-sm fixed w-full z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16">
        <!-- Logo -->
        <div class="flex items-center">
          <NuxtLink to="/" class="text-2xl font-bold text-blue-600">
            MyBrand
          </NuxtLink>
        </div>

        <!-- Desktop Menu -->
        <div class="hidden md:flex items-center space-x-6">
          <NuxtLink to="/" class="text-gray-700 hover:text-blue-600 transition">Home</NuxtLink>
          <NuxtLink to="/about" class="text-gray-700 hover:text-blue-600 transition">About</NuxtLink>
          <NuxtLink to="/services" class="text-gray-700 hover:text-blue-600 transition">Services</NuxtLink>
          <NuxtLink to="/contact" class="text-gray-700 hover:text-blue-600 transition">Contact</NuxtLink>
          <button class="ml-4 bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition">
            Get Started
          </button>
        </div>

        <!-- Mobile Menu Button -->
        <div class="flex items-center md:hidden">
          <button @click="isOpen = !isOpen" class="p-2 text-gray-700 hover:text-blue-600 focus:outline-none">
            <svg
              v-if="!isOpen"
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16" />
            </svg>
            <svg
              v-else
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div v-if="isOpen" class="md:hidden bg-white border-t border-gray-200">
      <div class="px-4 py-3 space-y-2">
        <NuxtLink to="/" class="block text-gray-700 hover:text-blue-600">Home</NuxtLink>
        <NuxtLink to="/about" class="block text-gray-700 hover:text-blue-600">About</NuxtLink>
        <NuxtLink to="/services" class="block text-gray-700 hover:text-blue-600">Services</NuxtLink>
        <NuxtLink to="/contact" class="block text-gray-700 hover:text-blue-600">Contact</NuxtLink>
        <button class="w-full bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition">
          Get Started
        </button>
      </div>
    </div>
  </nav>

  <main class="container">
    <slot />
  </main>
</template>

<script setup>
import { ref } from 'vue'

const isOpen = ref(false)
</script>
