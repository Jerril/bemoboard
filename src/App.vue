<template>
  <div id="app">
      <Navbar />
      <Board :columns="columns" />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Board from './components/Board.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Board
  },
  data() {
    return {
      columns: [
        {
          id: 1,
          title: "col1",
          cards: [
            {
              id: 10,
              title: "hello world",
              description: "hello people. Hope you'll are good",
              position: 1,
              active: true
            },
            {
              id: 10,
              title: "hello world",
              description: "hello people. Hope you'll are good",
              position: 1,
              active: true
            }
          ]
        },
        {
          id: 2,
          title: "col2",
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 0 
}
</style>
