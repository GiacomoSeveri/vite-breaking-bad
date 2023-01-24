<script>
import PokemonList from '../components/pokemon/PokemonList.vue';
export default {
    name: 'AppMain',
    components: { PokemonList }

};
</script>

<template>
    <main class="container">
        <pokemon-list class="mb-3"></pokemon-list>
    </main>
</template>

<style>

</style>