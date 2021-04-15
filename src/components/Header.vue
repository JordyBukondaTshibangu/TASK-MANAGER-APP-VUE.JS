<template>
    <header>
        <h1>{{title}}</h1>
        <Button text="Add Task" color="green" @show-task="$emit('show-task')"/>
    </header>
</template>

<script>

import Button from './Button.vue';

export default {
    name : 'Header',
    components : {
        Button : Button
    },
    props : {
        title : {
            type : String,
            default : "Task Manager app"
        }
    },
    methods : {
    }
}
</script>
<style scoped>
    header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
    }
</style>