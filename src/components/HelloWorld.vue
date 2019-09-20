<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      board: [ 
        [
          [0,0,null],
          [0,1,null],
          [0,2,null]
        ],
        [
          [1,0,null],
          [1,1,null],
          [1,2,null]
        ],
        [
          [2,0,null],
          [2,1,null],
          [2,2,null]
        ]
      ],
    };
  },
  props: {
    msg: String
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
</style>
