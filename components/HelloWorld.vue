<template>
  <div>
    {{message}}
  </div>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator'

@Component
export default class HelloWorld extends Vue {
  message = 'Hello world :)'
}
</script>
