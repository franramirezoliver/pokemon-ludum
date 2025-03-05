<template>
  <ul>
    <li>Pokèmon 1</li>
    <li>Pokèmon 2</li>
    <li>Pokèmon 3</li>
    <li>Pokèmon 4</li>
  </ul>
</template>

<script setup lang="ts"></script>

<style scoped>
@import 'tailwindcss';

li {
  @apply bg-white shadow-md rounded-lg p-3 my-2 cursor-pointer w-40 text-center hover:bg-gray-100 transition-all;
}
</style>
