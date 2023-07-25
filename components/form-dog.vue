<script lang="ts" setup>
import { Dog } from '../entities';


const emit =defineEmits <{
 (e: 'submitDog' , dog:Dog) :void 
}>();

const dog = ref<Dog>({
  name: "",
  breed: "",
  birthdate: "2023-01-01"
});


function onSubmit() {
  console.log(dog.value);
  emit('submitDog',dog.value);

}
</script>

<template>
  <form @submit.prevent="onSubmit()">
    <label for="name">Name</label>
    <input type="text" id="name" v-model="dog.name"><br>

    <label for="breed">Breed</label>
    <input type="text" id="breed" v-model="dog.breed"><br>

    <label for="birthdate">Birthdate</label>
    <input type="text" id="birthdate" v-model="dog.birthdate"><br>
    <button class="btn btn-info">ADD</button>
  </form>
</template>

<style scoped></style>
