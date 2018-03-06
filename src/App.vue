<template>
  <div id="app">
    <todo-app></todo-app>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import TodoApp from './components/TodoApp.vue';

@Component({
  components: {
    TodoApp,
    },
  })

export default class App extends Vue {}
</script>
