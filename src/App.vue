<template>
  <div id="app">
   <nav-bar />
   <router-view></router-view>

  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import AddCar from './pages/AddCar.vue'

export default {
  name: 'app',
  components: {
    NavBar,
    AddCar
  }
}
</script>
