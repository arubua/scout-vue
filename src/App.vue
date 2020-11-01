<template>
 <div id="main">
   <DraftList v-bind:players="players" />
 </div>
</template>

<script>
import DraftList from './components/DraftList.vue'

export default {
  name: 'App',
  components: {
    DraftList
  },
  data() {
    return {
      players: [
        {
          name: "Maxwell Mulili",
          age: "19",
          drafted: true
        },
        {
          name: "Boniface Mwangemi",
          age: "20",
          drafted: false
        },
        {
          name: "Omar Somobwana",
          age: "17",
          drafted: true
        },
        {
          name: "Nicholas Omondi",
          age: "18",
          drafted: false
        },
        {
          name: "Enock Wanyama",
          age: "18",
          drafted: true
        },
        {
          name: "Telvin Maina ",
          age: "19",
          drafted: false
        },
        {
          name: "Henry Meja",
          age: "19",
          drafted: true
        },
        {
          name: "ellasie Otieno",
          age: "17",
          drafted: false
        },
        {
          name: "Mwakio Kisaka",
          age: "18",
          drafted: true
        },
        {
          name: "Timothy Ouma",
          age: "19",
          drafted: false
        }
      ]
    }
  }
}
</script>

<style>
#main{
  margin: auto;
  width: 50%;
  display: table;
}
</style>
