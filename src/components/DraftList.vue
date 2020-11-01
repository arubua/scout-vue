<template>
    <h1>Draft List</h1>
    
    <div class="left">
        <h3>Drafted</h3>
        <div v-bind:key="player.id" v-for=" player in players" v-bind:class="{'is-drafted':player.drafted}" >
            <Drafted v-bind:player="player" v-if="player.drafted"/>
        </div>
        <h3>Total Age is: {{totalDrafted}}</h3>
    </div>
    <div class="right">
        <h3>Not Drafted</h3>
        <div v-bind:key="player.id" v-for=" player in players" v-bind:class="{'not-drafted':!player.drafted}">
            <NotDrafted v-bind:player="player" v-if="!player.drafted"/>
        </div>
        <h3>Total Age is: {{totalNotDrafted}}</h3>
    </div> 
</template>

<script>
import Drafted from "./Drafted.vue";
import NotDrafted from "./NotDrafted.vue";

export default {
    name: "DraftList",
    components: {
        Drafted,
        NotDrafted
    },
    props: ["players"],
    computed: {
    totalDrafted: function() {
    let total = 0;
    for(let i = 0; i < this.players.length; i++){
        if(this.players[i].drafted){
            total += parseInt(this.players[i].age);
        }
    }
    return total;
  },
  totalNotDrafted: function() {
    let total = 0;
    for(let i = 0; i < this.players.length; i++){
        if(!this.players[i].drafted){
            total += parseInt(this.players[i].age);
        }
    }
    return total;
  }
  
}
}
</script>

<style scoped>
.left{
    float: left;
}
.right{
   float: right; 
}
.is-drafted{
    color: green;
}
.not-drafted{
    color: red;
}
</style>