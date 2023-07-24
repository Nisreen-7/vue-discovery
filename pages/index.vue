<script lang="ts" setup>
const first=ref('test');
function changFirst(){
  first.value='autre chose';
}

</script>

<template>
  <div>
   {{first}}
  </div>
  <button @click="changFirst()" class="btn btn-info"> click !</button>
</template>

<style scoped></style>
