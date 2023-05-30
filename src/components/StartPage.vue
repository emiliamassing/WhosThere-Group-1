<script setup lang="ts">
    import { ref } from 'vue';
    import { arrayOfAnimals } from '../data/Animals';
    import Gameboard from '../components/GameBoard.vue';

    let gameStarted = ref(false);
    console.log(gameStarted);

    function startGame() :void {
        gameStarted.value = true;
        console.log(gameStarted);
        randomizeAnimal();
    };

    function randomizeAnimal() {
        const randomAnimal = arrayOfAnimals[Math.floor(Math.random()*arrayOfAnimals.length)];
        console.log(randomAnimal);
        
        return randomAnimal;
    };
</script>

<template>
    <div v-if="!gameStarted">
        <h2>Who's There? - Animal edition</h2>
        <button @click="startGame">Start game</button>
    </div>
    <template v-else>
        <Gameboard></Gameboard>
    </template>
</template>


<style>
    h2{
        margin-bottom: 1em;
    }
    
</style>