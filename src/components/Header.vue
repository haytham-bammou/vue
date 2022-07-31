<template>
    <header>
        <h1>{{title}}</h1>
        <Button @click="$emit('show-AddTask')" :text="showAddTask ?  'close' : 'Add Task'" :color="showAddTask ?  'red' : 'green'"/>
    </header>
</template>

<script>
    import Button from './Button.vue'; 
    export default {
        name: "header",
        props : {
            title : {
                type : String ,
                default : "default "
            },
            showAddTask : Boolean,
        },
        components : {
            Button
        },
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