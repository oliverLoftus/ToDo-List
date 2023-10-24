<!-- src/components/ToDoList.vue -->
<templates>
  <div>
    <h1>ToDo list</h1>
    <ul>
      <li v-for="(todo, index) in todos" :key="index">
        {{todo}}
        <button @click="removeTodo(index)">Remove</button>
      </li>
     </ul>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const todos = ref ([]);

    const removeTodo = (index) => {
      todos.value.splice(index, 1);
    };

    return {
      todos,
      removeTodo,
    };
  },
};
</script>