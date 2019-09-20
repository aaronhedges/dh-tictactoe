<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.

      <!-- {{ this.board }} -->
    </p>
    <div class="board">
      <div class="row" v-for='row in board'>
        <button 
          class="cell" 
          v-for='cell in row'
          v-on:click='playerMove(cell)'
        >
          {{ cell.slice(2).toString() }}
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      board: [ 
        [
          [0,0,'x'],
          [0,1,'o'],
          [0,2,'x']
        ],
        [
          [1,0,'o'],
          [1,1,'x'],
          [1,2,'o']
        ],
        [
          [2,0,'o'],
          [2,1,'o'],
          [2,2,'x']
        ]
      ],
    };
  },
  props: {
    msg: String
  },
  methods: {
    playerMove: function (cell) {
      alert('player move made')
      alert(cell)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.board {
  max-width: 200px;
}
.row {
   
} 
.cell {
  padding: .5em;
}


</style>
