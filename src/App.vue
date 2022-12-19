<template>
    <div class="app">
        <p>{{ jobs[0].location }}</p>
    </div>
</template>


<script setup lang="ts">
    import { ref } from 'vue';
    import Job from './types/Job';

    const jobs = ref<Job[]>([
        { id: '1', title: 'Farm Worker' , location: 'Lon Lon Ranch' , salary  : 30000 },
        { id: '2', title: 'Quarryman'   , location: 'Death Mountain', salary  : 40000 },
        { id: '3', title: 'Flute Player', location: 'The Lost Woods', salary  : 35000 },
        { id: '4', title: 'Fisherman'   , location: 'Lake Hylia'    , salary  : 21000 },
        { id: '5', title: 'Prison Guard', location: 'Gerudo Valley' , salary  : 32000 }
    ]);
</script>


<style scoped>

</style>
