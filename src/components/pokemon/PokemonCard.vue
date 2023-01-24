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
    <div class="text-center custom-card">
        <img :src="image" :alt="name">
        <h4 type="button"><strong>{{ name }}</strong></h4>
        <p><strong>{{ number }}</strong></p>
        <span class="fs-4">{{ type1 }} {{ type2 }}</span>
    </div>
</template>

<style>
img {
    width: 200px;
    height: 200px;
    object-fit: contain;
    /* border-radius: 50%; */
    cursor: pointer;
    margin-bottom: 5px;
    border-bottom: #C52919 solid 1px;
}

.custom-card {
    border: solid 1px #C52919;
    padding: 5px;
    background-color: #fff;
    color: #000;
    border-radius: 5px;
}
</style>