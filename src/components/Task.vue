<template>
  <li>
    <div>{{task.name}} {{index}}</div>
    <small>{{task.dueDate}} @ {{task.dueTime}}</small>
    <button @click="deleteTask()">X</button>
  </li>
</template>

<script>

export default {
  props: ['task', 'index'],
  methods: {
    deleteTask () {
      this.$emit('deleteTask', this.index) /* the emit method connects the deleteTask method from Index.vue
      to here */
    }
  }
}
</script>

<style>
</style>
