<script setup lang="ts">
    import { ref } from 'vue';

    let gameStarted = ref(false);
    console.log(gameStarted);

    function startGame() :void {
        gameStarted.value = true;
        console.log(gameStarted);
    };
</script>

<template>
    <h2>Who's There? - Animal edition</h2>
    <button @click="startGame">Start game</button>
</template>

<style>
    h2{
        margin-bottom: 1em;
    }
    
</style>