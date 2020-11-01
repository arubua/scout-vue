<template >
    <li>
        {{player.name}}
        {{player.age}}
    </li>
</template>

<script>
export default {
    name:"Drafted",
    props: ["player"]
}
</script>

<style scoped>
 li{
    list-style: none; 
 }
</style>