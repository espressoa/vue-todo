<template>
  <div>
      <input type="text" v-model="newTodoItem"> <!-- input에 등록된 텍스트 값을 동적으로 -->
      <button v-on:click="addTodo">add</button>
  </div>
</template>

<script>
export default {
    data: function() {
        return {
            newTodoItem: ""
        }
    },
    methods: {
        addTodo: function() {
            localStorage.setItem(this.newTodoItem, this.newTodoItem);
            this.newTodoItem = '';
        }
    }
}
</script>

<style>

</style>