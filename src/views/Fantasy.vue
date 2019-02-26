<template>
    <section class="screen --divisions">
          <div class="screen__table">
            <div class="screen__cards">
                <div class="screen__card">
                    <FreeAgents :players='players'/>
                </div>
            </div>
        </div>
    </section>
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
