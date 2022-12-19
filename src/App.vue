<template>
    <div class="app">
        <p>Name: {{ name }}</p>
        <p>Age: {{ age }}</p>
        <button @click="changeName('Link')">Change Name</button>
        <button @click="changeAge(29)">Change Age</button>
    </div>
</template>


<script lang="ts">
    import { defineComponent } from 'vue';

    export default defineComponent({
        name: 'App',
        components: {},
        data() {
            return {
                name: 'Hyper',
                age : 25 as number | string
            }
        },
        methods: {
            changeName(newName: string) {
                this.name = newName;
                return name;
            },
            changeAge(age: string | number) {
                this.age = age;
                return age;
            }
        }
    });
</script>


<style scoped>

</style>
