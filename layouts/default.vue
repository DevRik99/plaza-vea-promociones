<template>
  <div class="grid grid-cols-1 lg:grid-cols-2 h-screen relative">
    <div
      class="h-full object-center w-full object-cover hidden lg:block sticky top-0 left-0"
    >
      <img
        src="/img/fondo.png"
        class="h-screen object-center w-full object-cover hidden lg:block sticky top-0 left-0"
        alt="Plaza Vea"
      />
    </div>
    <nuxt-link to="/" class="flex items-center justify-center block lg:hidden p-5">
      <img src="/img/logo.png" alt="Plaza Vea" />
    </nuxt-link>
    <NuxtPage />
  </div>
</template>

<script setup></script>
