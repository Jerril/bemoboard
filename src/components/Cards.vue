<template>
    <div id="cards">    
        <div class="card" :key="card.id" v-for="card in cards">
            <p>{{card.title}}</p>
        </div>
    </div>
</template>
<script>
export default {
    name: "Cards",
    props: {
        cards: Array
    }
}
</script>
<style>
    #cards .card {
        background-color: #fff;
        border-radius: 5px;
        padding: 10px;
        margin-bottom: 10px;
    }
</style>