<script setup lang="ts">
import { IAnimal } from '../models/IAnimal';
import { IAnimalDesc } from '../models/IAnimalDesc';


const arrayOfAnimals: IAnimal = [
    {
        name: 'Zebra',
        picture: './assets/zebra.png',
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
        picture: './assets/deer.png',
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
        picture: './assets/elephant.png',
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
        picture: './assets/giraffe.png',
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
        picture: './assets/leo.png',
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
        picture: './assets/monkey.png',
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
        picture: './assets/panda.png',
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
        picture: './assets/rhino.png',
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
        picture: './assets/tiger.png',
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
]

</script>

<template>
    <div><img :src=""></div>
</template>

<style>

</style>