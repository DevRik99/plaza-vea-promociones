<script setup>
const page = ref(1);
const promociones = ref([]);
const getPromociones = async () => {
  try {
    const response = await fetch(
      `https://61c35faa9cfb8f0017a3eb2e.mockapi.io/api/v1/posts/?page=${page.value}&limit=10`
    );
    const data = await response.json();
    promociones.value = [...promociones.value, ...data.items];
  } catch (error) {
    console.log(error);
  }
};
const onScroll = (event) => {
  page.value += 1;
  getPromociones();
};
onMounted(() => {
  getPromociones();
});
</script>
<template>
  <div class="m-[45px] scroll-auto">
    <h2 class="text-[#FC2016] font-bold text-2xl my-6">Todas las promociones</h2>
    <section class="flex flex-col justify-center items-start gap-5 mx-auto">
      <p class="mx-auto font-medium w-full">Últimas promociones</p>

      <Promocion
        v-for="({ image, title, id, description }, index) of promociones"
        :key="index"
        :url="image"
        :title="title"
        :id="id"
        :description="description"
      />
    </section>
  </div>
</template>
