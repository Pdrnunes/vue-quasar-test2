<template>
  <q-page padding>
    <ul>
      <li v-for="task in tasks" :key="task">
        {{task}}
      </li>
    </ul>
  </q-page>
</template>

<script>
export default {
  data () {
    return {
      tasks: ['Go to the market', 'buy crackers', 'buy butter']
    }
  }
}
</script>

|<style>
</style>
