<script>
export default {
    name: 'PokemonCard',
    props: {
        name: String,
        image: String,
        number: Number,
        type1: String,
        type2: String,
    }
};
</script>

<template>
    <div class="text-center">
        <img :src="image" alt="name">
        <h4>{{ name }}</h4>
        <p>{{ number }}</p>
        <span>{{ type1 }} {{ type2 }}</span>
    </div>
</template>

<style>

</style>