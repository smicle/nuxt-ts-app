<template>
  <div>
    <h1>{{message}}</h1>
  </div>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator'

@Component
export default class TodosList extends Vue {
  message: string = 'Todo List 😎'
}
</script>
