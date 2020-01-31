<template>
  <div class="flex flex-wrap">
    <div class="w-full md:w-1/2 lg:w-1/3 px-3 py-5" v-for="(character, index) in characters" :key="index">
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