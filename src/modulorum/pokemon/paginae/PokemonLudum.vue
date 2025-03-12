<template>
  <section
    v-if="estPortat || temerePokemon.id === null"
    class="flex justify-center items-center flex-col w-screen h-screen"
  >
    <h1 class="text-3xl">Espere, por favor</h1>
    <h3 class="animate-pulse">Cargando Pokémons</h3>
  </section>

  <section v-else class="flex justify-center items-center flex-col w-screen h-screen">
    <h1 class="m-5">¿Quién es este Pokémon?</h1>
    <!-- <h3>{{ temerePokemon }}</h3> -->
    <h3 class="capitalize my-3">{{ ludumStatus }}</h3>
    <PokemonImago
      :pokemon-id="temerePokemon.id"
      :revelare-pokemon="ludumStatus !== LudumStatus.Ludit"
    />
    <PokemonOptiones :optiones="optiones" @electus-optio="examineResponsio" />
  </section>
</template>

<script setup lang="ts">
import PokemonImago from '../components/PokemonImago.vue';
import PokemonOptiones from '../components/PokemonOptiones.vue';
import { usePokemonLudum } from '../composables/usePokemonLudum';
import { LudumStatus } from '../interfaces';

const {
  ludumStatus,
  estPortat,
  temerePokemon,
  pokemonOptiones: optiones,
  examineResponsio,
} = usePokemonLudum();

// const cumElectusOptio = (valorem: number) => {
//   console.log(valorem);
// };
</script>

<style scoped></style>
