<script lang="ts" setup>
import { Dog } from 'entities';

const {data,refresh} =await useFetch<Dog[]>('http://localhost:8000/api/dog');


async function addDog(dog:Dog){
  await $fetch('http://localhost:8000/api/dog' ,{
    method:'POST',
    body:dog
  });
  refresh();
}
</script>

<template>
  <h4>avant component</h4>
 <p v-for="item of data">{{ item.name }}</p>

 <h4>apres de creer le component</h4>

 <DogItem v-for="item of data" :dog="item"/>

 <FormDog @submitDog="addDog($event)"/>
</template>

<style scoped></style>
