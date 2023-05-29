<script setup lang="ts">
import { IAnimal } from '../models/IAnimal';
import { IAnimalDesc } from '../models/IAnimalDesc';


const arrayOfAnimals: IAnimal[] = [
    {
        name: 'Zebra',
        picture: '../src/assets/zebra.png',
        description: {
            Stripes: true,
            Tail: true,
            Hooves: true,
            Spots: false,
            Tall: false,
            Horns: false,
            Brown: false,
            Paws: false,
            Fur: true,
            Mane: true,
            Horn: false,
            Grey: false,
            Furless: false,
            Trunk: false,
            Heavy: false,
            Monochrome: false,
            Climber: false
        },
    },
    {
        name: 'Deer',
        picture: '../src/assets/deer.png',
        description: {
            Stripes: false,
            Tail: true,
            Hooves: false,
            Spots: false,
            Tall: false,
            Horns: true,
            Brown: true,
            Paws: false,
            Fur: true,
            Mane: true,
            Horn: false,
            Grey: false,
            Furless: false,
            Trunk: false,
            Heavy: false,
            Monochrome: false,
            Climber: false
        }
    },
    {
        name: 'Elephant',
        picture: '../src/assets/elephant.png',
        description: {
            Stripes: false,
            Tail: true,
            Hooves: false,
            Spots: false,
            Tall: true,
            Horns: false,
            Brown: false,
            Paws: false,
            Fur: false,
            Mane: false,
            Horn: false,
            Grey: true,
            Furless: true,
            Trunk: true,
            Heavy: true,
            Monochrome: true,
            Climber: false
        }
    },
    {
        name: 'Giraffe',
        picture: '../src/assets/giraffe.png',
        description: {
            Stripes: false,
            Tail: true,
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
            Trunk: true,
            Heavy: true,
            Monochrome: false,
            Climber: false
        },
    },
    {
        name: 'Leo',
        picture: '../src/assets/leo.png',
        description: {
            Stripes: false,
            Tail: true,
            Hooves: false,
            Spots: false,
            Tall: false,
            Horns: false,
            Brown: false,
            Paws: true,
            Fur: true,
            Mane: true,
            Horn: false,
            Grey: false,
            Furless: false,
            Trunk: false,
            Heavy: false,
            Monochrome: false,
            Climber: false
        }
    },
    {
        name: 'Monkey',
        picture: '../src/assets/monkey.png',
        description: {
            Stripes: false,
            Tail: false,
            Hooves: false,
            Spots: false,
            Tall: false,
            Horns: false,
            Brown: true,
            Paws: false,
            Fur: true,
            Mane: false,
            Horn: false,
            Grey: false,
            Furless: false,
            Trunk: false,
            Heavy: false,
            Monochrome: false,
            Climber: true
        } 
    },
    {
        name: 'Panda',
        picture: '../src/assets/panda.png',
        description: {
            Stripes: false,
            Tail: false,
            Hooves: false,
            Spots: false,
            Tall: false,
            Horns: false,
            Brown: false,
            Paws: true,
            Fur: true,
            Mane: false,
            Horn: false,
            Grey: false,
            Furless: false,
            Trunk: false,
            Heavy: false,
            Monochrome: false,
            Climber: false
        } 
    },
    {
        name: 'Rhino',
        picture: '../src/assets/rhino.png',
        description: {
            Stripes: false,
            Tail: true,
            Hooves: false,
            Spots: false,
            Tall: false,
            Horns: false,
            Brown: false,
            Paws: false,
            Fur: false,
            Mane: false,
            Horn: true,
            Grey: true,
            Furless: true,
            Trunk: false,
            Heavy: true,
            Monochrome: true,
            Climber: false
        } 
    },      
    {
        name: 'Tiger',
        picture: '../src/assets/tiger.png',
        description: {
            Stripes: true,
            Tail: true,
            Hooves: false,
            Spots: false,
            Tall: false,
            Horns: false,
            Brown: false,
            Paws: true,
            Fur: true,
            Mane: false,
            Horn: false,
            Grey: false,
            Furless: false,
            Trunk: false,
            Heavy: false,
            Monochrome: false,
            Climber: true
        }
    }                
];

const gridClass: string ="gridContainer";

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
        <option>Fur</option>
        <option>Trunk</option>
        <option>Tail</option>
        <option>Paws</option>
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