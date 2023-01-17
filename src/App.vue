<template>
  <header></header>
  <main>
    <todolist />
  </main>
  <footer></footer>
  
</template>

<script>
import todolist from './components/todolist.vue'
import css from './assets/css/style.css'

export default {
  name: 'App',
  components: {
    todolist
  }
}
</script>
