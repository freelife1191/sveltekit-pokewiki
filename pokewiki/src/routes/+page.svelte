<script>
  import {arrPokemon} from "../stores/pokestore";
  // console.log($arrPokemon)
  import PokemonCard from '../components/pokemonCard.svelte'

  let searchTerm = ''
  let filterPokemon = []

  // reactivity
  $: {
    console.log(searchTerm)
    if (searchTerm) {
      filterPokemon = $arrPokemon.filter((pokemon) => pokemon.name.includes(searchTerm))
    } else {
      filterPokemon = [...$arrPokemon]
    }
  }
</script>

<svelte:head>
  <title>포켓몬 위키</title>
</svelte:head>

<h1 class="text-4xl text-center my-8 font-bold underline">
  포켓몬 위키 사이트
</h1>

<input class="w-full rounded-md text-lg p-4 mb-8 border-2 border-gray-200"
       type="text"
       bind:value={searchTerm}
       placeholder="포켓몬 검색"/>

<div class="grid gap-4 md:grid-cols-3 grid-cols-2">
  {#each filterPokemon as pokemon}
    <PokemonCard {pokemon}/>
  {/each}
</div>