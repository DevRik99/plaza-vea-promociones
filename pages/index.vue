<script setup>
const router = useRouter();
const registerUser = () => {
  console.log("reg");
  router.push("/promociones");
};
</script>
<template>
  <form class="m-[45px]" @submit.prevent="registerUser">
    <h2 class="text-[#FC2016] font-bold text-2xl my-6">Registrate para ingresar</h2>
    <section class="flex flex-col justify-center items-center gap-5 w-[294px] mx-auto">
      <p class="mx-auto font-medium w-full text-center">Foto de perfil</p>
      <div class="w-[160px] h-[160px] rounded-full bg-[#D9D9D9] my-[30px]"></div>
      <div>
        <label for="Nombres" class="text-base font-[400]">Nombres</label>
        <input
          type="text"
          class="bg-[#D9D9D9] w-full rounded p-2 mb-2"
          placeholder="Rodrigo"
          required
        />
        <label for="Apellidos" class="text-base font-[400]">Apellidos</label>
        <input
          type="text"
          class="bg-[#D9D9D9] w-full rounded p-2 mb-2"
          placeholder="Fernandez Panta"
          required
        />
        <button
          to="/promociones"
          class="bg-[#FFE81E] text-[#FC2016] w-full p-2 rounded-[40px] mt-[30px] text-center font-bold"
        >
          Ingresar
        </button>
      </div>
    </section>
  </form>
</template>

<script setup></script>
