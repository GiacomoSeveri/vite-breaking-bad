<script>
import PokemonCard from './PokemonCard.vue';

import axios from 'axios';
export default {
    name: 'PokemonList',
    components: { PokemonCard },
    data() {
        return {
            pokemon: []
        }
    },
    created() {
        axios.get('https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=10&page=47')
            .then(res => {
                this.pokemon = res.data.docs;
            });
    }
};
</script>

<template>
    <section id="pokemon">
        <div class="row">
            <pokemon-card v-for="pok in pokemon" :kay="pok._id" :name="pok.name" :image="pok.imageUrl"
                :number="pok.number" :type1="pok.type1" :type2="pok.type2"></pokemon-card>
        </div>
    </section>
</template>

<style>

</style>