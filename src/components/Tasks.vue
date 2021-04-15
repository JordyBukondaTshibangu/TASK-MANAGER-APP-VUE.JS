<template>
    <div>
        <div v-for="task in tasks" :key="task.id">
            <Task :task="task" @delete-task="$emit('delete-task', task.id)" />
        </div>
    </div>
</template>

<script>

import Task from './Task';

export default {
    name : "Tasks",
    props : {
        tasks : Array
    },
    components : {
        Task : Task
    },
    methods : {
        
    },
    emits : ['delete-task']
}
</script>