<template>
  <div class="hello">
    <input type="text" v-model="input" />
    <button @click="addTodo">add</button>
    <ul>
      <li v-for="(todo, i) in todos" :key="i">{{ todo.text }}</li>
    </ul>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class TodoApp extends Vue {
  todos = [{text: 'hoge', done: false}, {text: 'fuga', done: false}]
  input = ''
  addTodo() :void {
    if (this.input !== '')
    this.todos.push({ text: this.input, done: false })
    this.input = ''
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
