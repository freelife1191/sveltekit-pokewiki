<script>
  import {arrPokemon} from "../stores/pokestore.js";
  // console.log($arrPokemon)
  import PokemonCard from '../components/pokemonCard.svelte'
</script>

<svelte:head>
  <title>포켓몬 위키</title>
</svelte:head>

<h1 class="text-4xl text-center my-8 font-bold underline">
  포켓몬 위키 사이트
</h1>

<div class="grid gap-4 md:grid-cols-3 grid-cols-2">
  {#each $arrPokemon as poketmon}
    <PokemonCard pokemon={poketmon}/>
  {/each}
</div>