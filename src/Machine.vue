<template>
  <div id="app">
    <img src='./assets/singe.jpg'>
    <h1>{{ msg }}</h1>
    <br>
    <ul>
      <li v-for="machine in machines" :key="machine.id">
        {{ machine.id }} : {{ machine.name }} <toggle-button v-model="machine.status" v-on:click="machine.status=true"/> Status: {{ machine.status }}
      </li>
    </ul>

  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'La machine du jour...'
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