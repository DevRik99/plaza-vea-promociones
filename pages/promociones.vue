<template>
  <div class="m-[45px]">
    <h2 class="text-[#FC2016] font-bold text-2xl my-6">Registrate para ingresar</h2>
    <section class="flex flex-col justify-center items-center gap-5 w-[294px] mx-auto">
      <p class="mx-auto font-medium w-full text-center">Foto de perfil</p>
      <div class="w-[160px] h-[160px] rounded-full bg-[#D9D9D9] my-[30px]"></div>
      <form @submit.prevent="">
        <label for="Nombres" class="text-base font-[400]">Nombres</label>
        <input
          type="text"
          class="bg-[#D9D9D9] w-full rounded p-2 mb-2"
          placeholder="Rodrigo"
        />
        <label for="Apellidos" class="text-base font-[400]">Apellidos</label>
        <input
          type="text"
          class="bg-[#D9D9D9] w-full rounded p-2 mb-2"
          placeholder="Fernandez Panta"
        />
        <button
          type="button"
          class="bg-[#FFE81E] text-[#FC2016] w-full p-2 rounded-[40px] mt-[30px]"
        >
          Ingresar
        </button>
      </form>
    </section>
  </div>
</template>

<script setup></script>
