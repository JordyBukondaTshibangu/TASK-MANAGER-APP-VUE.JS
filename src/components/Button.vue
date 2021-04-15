<template>
    <button 
        :style="{background : color}" 
        class="btn"
        @click="$emit('show-task')"
        >
        {{text}}
    </button>
</template>
<script>
export default {
    name : 'Button',
    props : {
        text : String,
        color : String
    }
}
</script>