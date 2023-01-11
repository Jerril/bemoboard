<template>
    <div id="board">
        <div class="col" v-bind:key="column.id" v-for="column in columns">
            <p class="col__title">{{column.title}}</p>
            {{ columns.cards }} <Cards :cards="column.cards" />
            <button title="Add Card">+</button>
        </div>
    </div>
</template>
<script>
import Cards from './Cards.vue';

export default {
    name: "Board",
    components: {
        Cards
    },  
    props: {
        columns: Array
    }
}
</script>
<style>
    #board {
        display: flex;
        gap: 10px;
        overflow-x: scroll;
        padding: 15px 0;
    }

    #board .col {
        background-color: #F2F2F2;
        border-radius: 5px;
        padding: 10px;
        min-width: 250px;
    }

    #board .col__title {
        padding: 10px 0;
    }
</style>