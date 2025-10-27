<template>
  <section class="flex flex-col items-center justify-center min-h-screen text-center bg-gray-50">
    <h1 class="text-5xl font-extrabold text-gray-900 mb-4">
      Hello World 🌎
    </h1>
    <p class="text-lg text-gray-600 mb-8 max-w-md">
      Welcome to your Nuxt 4 + Tailwind 4 app! This page is rendered from <code>pages/index.vue</code>.
    </p>
    <NuxtLink
      to="/about"
      class="bg-blue-600 text-white px-6 py-3 rounded-xl hover:bg-blue-700 transition shadow-md"
    >
      Learn More
    </NuxtLink>
  </section>
</template>
