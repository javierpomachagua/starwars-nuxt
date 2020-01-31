<template>
  <div v-if="characters" class="flex justify-center flex-wrap items-center p-20">
    <div class="w-1/3 h-6 px-10" v-for="(character, index) in characters" :key="index">
      <Character :character="character"></Character>
    </div>      
  </div>
</template>

<script>
import Character from "./Character.vue";
import data from '@/assets/data/characters.json';

export default {
  name: "CharacterList",
  components: {
    Character
  },
  data() {
    return {
      characters: null
    }
  },
  created() {
    this.characters = data;
    console.log(this.characters);
  }
};
</script>

<style>
</style>