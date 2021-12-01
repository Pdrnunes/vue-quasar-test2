<template>
  <q-page padding>
    <ul>
      <li v-for="(task, index) in tasks" :key="task">
        <div>{{task.name}} {{index}}</div>
        <small>{{task.dueDate}} @ {{task.dueTime}}</small>
        <button @click="deleteTask(index)">X</button>
      </li>
    </ul>
  </q-page>
</template>

<script>
export default {
  data () {
    return {
      tasks: [
        {
          name: 'Go to the market',
          dueDate: '2021/12/01',
          dueTime: '19:56'
        },
        {
          name: 'Go to the bank',
          dueDate: '2021/12/02',
          dueTime: '14:00'
        },
        {
          name: 'Go to the beach',
          dueDate: '2021/12/03',
          dueTime: '9:15'
        }
      ]
    }
  },
  methods: {
    deleteTask (index) {
      this.tasks.splice(index, 1) /*  splice JSmethod removes an item from the array
                                      by passing it's position(index) and how much items will be deleted */
    }
  }
}
</script>

|<style>
</style>
