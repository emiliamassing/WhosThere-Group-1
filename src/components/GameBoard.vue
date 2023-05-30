<script setup lang="ts">
import { ref } from 'vue';
import { arrayOfAnimals } from '../data/Animals';
import { IAnimal } from '../models/IAnimal';

interface Animal {
    description: IAnimal;
}

const gridClass: string ="gridContainer";

const props = defineProps<Animal>();

const selectedQuestion = ref('');

const descriptionOptions: string[] = [
    'Stripes',
    'Tail',
    'Hooves',
    'Spots',
    'Tall',
    'Horns',
    'Brown',
    'Paws',
    'Fur',
    'Mane',
    'Horn',
    'Grey',
    'Furless',
    'Trunk',
    'Heavy',
    'Monochrome',
    'Climber'
];

function askQuestion() {
    let randomizedAnimalDescription = props.description.description;
    if(selectedQuestion.value in randomizedAnimalDescription) {
     console.log("du hade rätt!");
     
    }
    else {
        console.log("Du hade fel!");
        
    }
    randomizedAnimalDescription
    console.log('description from rando animal', props.description.description);
    console.log('selected question', selectedQuestion.value);
}

</script>

<template>
    <h3>Who's There? - Animal Edition</h3>
    <div :class="gridClass">
        <div v-for="animal in arrayOfAnimals" v-bind:key="animal.name" class="animal">
            <img :src="animal.picture">
            <h3>{{ animal.name }}</h3>
        </div>
    </div>
    <ul>
        <li>Fur: No</li>
        <li>Tail: Yes</li>
        <li>Paws: Yes</li>
    </ul>
    <h4>Does the animal have: </h4>
    <select v-model="selectedQuestion">
        <option v-for="description in descriptionOptions" :value="description" :key="description">{{ description }}</option>
    </select><br>
    <span>{{ selectedQuestion }}</span>
    <button @click="askQuestion">Ask Question</button>
</template>

<style>
    .gridContainer {
        display: grid;
        grid-template-columns: repeat(3, 350px);
        grid-template-rows: repeat(3, 350px);
    }

    .gridContainer .animal {
        border: 1px solid black;
    }

    img {
        margin-top: 1rem;
    }

    li {
        list-style-type: none;
    }

    img:hover {
        cursor: pointer;
    }

    button {
        margin-top: 1em;
    }
</style>