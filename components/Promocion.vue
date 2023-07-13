<script setup>
const props = defineProps({
  title: String,
  url: String,
  description: String,
  id: {
    required: true,
    type: [Number, String],
  },
});
</script>
<template>
  <nuxt-link
    :to="`/promociones/${id}`"
    class="flex justify-between items-start gap-5 mb-8"
  >
    <!-- <img :src="url" class="h-full rounded" /> -->
    <img src="/img/tv.png" class="h-full rounded" />
    <section class="w-[240px]">
      <p class="font-medium">{{ title }}</p>
      <span>{{ description }}</span>
    </section>
  </nuxt-link>
</template>
