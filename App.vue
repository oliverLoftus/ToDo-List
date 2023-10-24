<!-- src/App.vue -->
<template>
    <div>
        <h1>Vue 3 ToDo App</h1>
        <add-todo />
        <to-do-list />
    </div>
</template>

<script>
import AddTodo from './components/AddToDo.vue';
import ToDoList from '.components/ToDoList.vue';

export default {
    components: {
        AddTodo,
        ToDoList,
    },
};
</script>