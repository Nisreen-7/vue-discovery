<script lang="ts" setup>
import { Dog } from 'entities';


const route = useRoute();

const { data } = useFetch<Dog>('http://localhost:8000/api/dog/' + route.params.id);

</script>

<template>
    <div v-if="data">

        <h1>{{ data.name }}</h1>
        <p>{{ data.breed }}</p>
        <p>{{ data.birthdate }}</p>
    </div>
</template>