<script setup>
const route = useRoute();
const id = route.params.id;
const datos = ref();
const active = ref(false);
const getPromocion = async () => {
  try {
    const response = await fetch(
      `https://61c35faa9cfb8f0017a3eb2e.mockapi.io/api/v1/posts/${id}`
    );
    const data = await response.json();
    datos.value = data;
  } catch (error) {
    console.log(error);
  }
};
onMounted(() => {
  getPromocion();
});
</script>
<template>
  <div class="m-[45px]" v-if="datos">
    <nuxt-link to="/promociones" class="text-[#FC2016] font-bold text-2xl my-6">
      <i class="bx bx-arrow-back"></i>{{ datos.title }}</nuxt-link
    >
    <img src="/img/tv-full.png" alt="TV FULL" class="my-[30px]" />
    <div class="flex items-center">
      <img src="/img/profile.png" alt="" />
      <p class="font-bold text-[20px]">
        {{ datos.user?.firstName }} {{ datos.user?.lastName }}
      </p>
    </div>
    <p class="mb-5">
      {{ datos.description }}
    </p>
    <p>Publicado a las 12:30AM</p>
    <div class="flex gap-2 mb-[30px]">
      <button
        type="button"
        class="bg-[#FC2016] text-white p-2 rounded-[40px] mt-[30px] text-center w-[240px] font-bold"
      >
        Reservar
      </button>
      <button
        @click="active = !active"
        type="button"
        class="bg-[#eaeaea] text-black p-2 px-4 rounded-[40px] mt-[30px] text-center font-medium"
      >
        16
        <i class="bx" :class="active ? 'bxs-heart text-[#FC2016]' : 'bx-heart'"></i>
      </button>
    </div>
    <section>
      <p class="text-base font-bold my-2">Comentarios</p>
      <section class="flex mb-[30px]">
        <img src="/img/profile.png" class="w-[48px] h-[48px] rounded-full" alt="" />
        <div>
          <p class="font-medium">Tom Holland</p>
          <span
            >Muchas gracias Indra, realmente me ayudaste con la compra de ese producto.
            Estoy muy feliz con la nueva tele para mi casa :3</span
          >
        </div>
      </section>
      <section class="flex mb-[30px]">
        <img src="/img/profile.png" class="w-[48px] h-[48px] rounded-full" alt="" />
        <div>
          <p class="font-medium">Tom Holland</p>
          <span
            >Muchas gracias Indra, realmente me ayudaste con la compra de ese producto.
            Estoy muy feliz con la nueva tele para mi casa :3</span
          >
        </div>
      </section>
    </section>
  </div>
</template>
