<template>
  <div id="app">
    <h3>{{title}}</h3>
<button class="btn btn-primary" @click="fetchCharacter">Test Fetch char</button>
  </div>
</template>



<script>
export default {
  name: 'app',
  data() {
    return {
      title: 'Generate Your Collection'
    }
  },
  methods: {
    fetchCharacter() {
      fetch('http://swapi.co/api/people',{
          method: 'GET',
        mode:"no-cors"
      }).then(response => console.log(response))
    }
  }
}

</script>
