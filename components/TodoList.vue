<template>
  <div>
    <ul v-for="todo in allTodos" :key='todo.id'>
      <li>
        <Todo :todo="todo" />
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator'
import Todo from '~/components/Todo.vue'
import {namespace} from 'vuex-class'
import * as todos from '~/store/modules/todos'

const Todos = namespace(todos.name)

@Component({
  components: {
    Todo
  }
})
export default class TodoList extends Vue {
  @Todos.Getter allTodos
}
</script>
