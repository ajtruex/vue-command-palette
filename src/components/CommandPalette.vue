<script setup>
import { ref } from "vue"

const commandFilterText = ref("")
const commandList = ref([
  { id: 123, title: "Command Title", alias: [], hotkeys: [] },
  { id: 456, title: "Command Title", alias: [], hotkeys: [] },
  { id: 789, title: "Command Title", alias: [], hotkeys: [] }

])
</script>

<template>
  <div class="command-palette">
    <h1>My Command Palette</h1>
    <input type="text" v-model="commandFilterText" />
    <ul>
      <li v-for="command in commandList" :key="command.id">
        {{ command.title }}
        {{ command.hotkeys }}
      </li>
    </ul>
  </div>
</template>



<style>
</style>
