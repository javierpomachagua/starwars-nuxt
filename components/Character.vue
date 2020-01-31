<template>
  <div class="shadow-lg bg-white rounded">
    <div class="flex">
      <div class="w-1/3 character-img">
        <img
          :src="`img/${character.path}`"
          class="object-cover w-full h-full"
          alt="character"
        />
      </div>
      <div class="w-2/3 p-4">
        <p class="text-2xl">{{ character.name }}</p>
        <p class="text-base text-gray-700">
          {{ character.description }}
        </p>
        <button
          class="float-right mt-3 bg-transparent text-black border border-yellow-500 hover:bg-yellow-500 hover:text-white rounded px-4 py-2"
        >
          Ver más
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Character",
  props: {
    character: {
      type: Object,
      required: true
    }
  }
};
</script>

<style>
</style>