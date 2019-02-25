<template>
    <div>
        <h1>Free Agents</h1>
        <Player v-for="(player, index) in freePlayers" :key="index" :name="player.name" />
    </div>
</template>

<script>
import Player from '@/components/Player';

export default {
    name: "FreeAgents",
    components: {
        Player
    },
    props: {
        players: Array
    },
    computed: {
        freePlayers() {
            return this.players.filter(player => !player.team.name)
        }
    }
}
</script>