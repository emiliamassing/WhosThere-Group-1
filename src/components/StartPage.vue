<script setup lang="ts">
    import { ref } from 'vue';
    import { arrayOfAnimals } from '../data/Animals';
    import Gameboard from '../components/GameBoard.vue';
import { IAnimal } from '../models/IAnimal';

    let gameStarted = ref(false);
    console.log(gameStarted);

    const randomizedAnimal = ref<IAnimal>({name: '', picture: '', description: {
        Stripes: false,
        Tail: false,
        Hooves: false,
        Spots: false,
        Tall: false,
        Horns: false,
        Brown: false,
        Paws: false,
        Fur: false,
        Mane: false,
        Horn: false,
        Grey: false,
        Furless: false,
        Trunk: false,
        Heavy: false,
        Monochrome: false,
        Climber: false 
    }});

    function startGame() :void {
        gameStarted.value = true;
        console.log(gameStarted);
        randomizeAnimal();
    };

    function randomizeAnimal() {
        const randomAnimal = arrayOfAnimals[Math.floor(Math.random()*arrayOfAnimals.length)];
        console.log(randomAnimal);
        
        randomizedAnimal.value = randomAnimal;
    };
</script>

<template>
    <div v-if="!gameStarted">
        <h2>Who's There? - Animal edition</h2>
        <button @click="startGame">Start game</button>
    </div>
    <template v-else>
        <Gameboard :description="randomizedAnimal"></Gameboard>
    </template>
</template>


<style>
    h2{
        margin-bottom: 1em;
    }
    
</style>