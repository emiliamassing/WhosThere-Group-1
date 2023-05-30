<script setup lang="ts">
import { arrayOfAnimals } from '../data/Animals';

const gridClass: string ="gridContainer";

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
    <select>
        <option v-for="description in descriptionOptions">{{ description }}</option>
    </select><br>
    <button>Ask Question</button>
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