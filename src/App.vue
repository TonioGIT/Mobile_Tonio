<template>
  <div id="app">
    <img src='./assets/singe.jpg'>
    <h1>{{ msg }}</h1>
    <br>
    <!-- <h2>Monkey machine #1: {{ machine1}}</h2>
    <h2>Monkey machine #2: {{ machine2}}</h2>
    <h2>Monkey machine #3: {{ machine3}}</h2> -->

    <ul>
      <li v-for="machine in machines">
        {{ machine.id }} : {{ machine.name }}
      </li>
    </ul>

    </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Mes machines à monkeys...',
      // machine1: 'Yvan l\'orang outan.',
      // machine2: 'Mac le macaque.',
      // machine3: 'Zézé le chimpanzé.',
      machines: [
        {id:1, name:'Yvan l\'orang outan.'},
        {id:2, name:'Mac le macaque.'},
        {id:3, name:'Zézé le chimpanzé.'}
      ]
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  // display: inline-block;
  margin: 50px;
  font-size: 30px;
}

a {
  color: #42b983;
}
</style>
