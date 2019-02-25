<template>
  <div class="home">
    <h1>Hello</h1>
    <FreeAgents :players='players' />
  </div>
</template>

<script>
// @ is an alias to /src
import FreeAgents from '@/components/FreeAgents'

export default {
  name: 'home',
  components: {
    FreeAgents
  },
  data(){
    return {
      players: []
    }
  },
  methods: {

  },
  created: function() {
    fetch(`http://localhost:4000/players`)
          .then(rsp => rsp.json())
          .then(data => {
              this.players = data;
          });
  }
}
</script>

<style lang="scss">

</style>
