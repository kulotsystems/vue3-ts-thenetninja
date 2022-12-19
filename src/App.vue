<template>
    <div class="app">
        <header>
            <div class="order">
                <button
                    @click="handleClick('title')"
                    :class="{ 'active': order === 'title' }"
                >
                    Order by Title
                </button>
                <button
                    @click="handleClick('salary')"
                    :class="{ 'active': order === 'salary' }"
                >
                    Order by Salary
                </button>
                <button
                    @click="handleClick('location')"
                    :class="{ 'active': order === 'location' }"
                >
                    Order by Location
                </button>
            </div>
        </header>

        <job-list :jobs="jobs" :order="order"/>
    </div>
</template>


<script setup lang="ts">
    import { ref } from 'vue';
    import Job from './types/Job';
    import OrderTerm from './types/OrderTerm';
    import JobList from './components/JobList.vue';

    const order = ref<OrderTerm>('title');

    const jobs = ref<Job[]>([
        { id: '1', title: 'Farm Worker' , location: 'Lon Lon Ranch' , salary  : 30000 },
        { id: '2', title: 'Quarryman'   , location: 'Death Mountain', salary  : 40000 },
        { id: '3', title: 'Flute Player', location: 'The Lost Woods', salary  : 35000 },
        { id: '4', title: 'Fisherman'   , location: 'Lake Hylia'    , salary  : 21000 },
        { id: '5', title: 'Prison Guard', location: 'Gerudo Valley' , salary  : 32000 }
    ]);

    const handleClick = (term: OrderTerm) => {
        order.value = term;
    };
</script>


<style scoped>
    header {
        text-align: center;
    }
    header .order {
        margin-top: 20px;
    }
    button {
        margin: 0 10px;
        color: #1195c9;
        border: 3px solid #43b4e0;
        background: #d5f0ff;
        padding: 8px 16px;
        border-radius: 4px;
        cursor: pointer;
        font-weight: bold;
        margin: 8px;
    }
    button.active {
        border: 3px solid #1195c9;
    }
</style>
