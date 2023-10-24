<!-- src/components/AddToDo.vue -->
<templates>
    <div>
        <h2>Add ToDo</h2>
        <input v-model="newTodo" @keyup.enter="addTodo" placeholder="Enter a new ToDo" />
        <button @click="addTodo">Add</button>
    </div>
</templates>

<script>
import { ref } from 'vue';

export default {
    setup() {
        const newTodo = ref('');
        const addTodo = () => {
            if (newTodo.value.trim() === '') return;
            todos.value.push(newTodo.value);
            newTodo.value = '';
        };

        return {
            newTodo,
            addTodo,
        };
    },
};
</script>