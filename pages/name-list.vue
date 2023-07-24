<script lang="ts" setup>
const names=ref(["nisreen","louna","abdullah"]);
const newName=ref('');

function addName(){
  names.value.push(newName.value);
}

</script>

<template>
  <div>
    <input type="text" v-model="newName" placeholder="type le nom">
    <button @click="addName()" class="btn btn-primary">Add</button>
   <ul >
    <li v-for="item of names">{{ item}}</li>
   </ul>
  </div>
</template>

<style scoped></style>
