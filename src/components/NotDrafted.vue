<template >
    
    <li>
        {{player.name}}
        {{player.age}}
    </li>
</template>

<script>
export default {
    name:"NotDrafted",
    props: ["player"]
}
</script>

<style scoped>
 li{
    list-style: none; 
 }
</style>