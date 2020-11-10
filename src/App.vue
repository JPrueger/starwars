<template>
  <div id="app">
    <Navbar/>
    <Characters/>
  </div>
</template>

<script>
import Characters from './components/Characters.vue'
import Navbar from '@/components/Navbar'

export default {
  name: 'App',
  components: {
    Characters,
    Navbar
  }
}
</script>

<style lang="scss" src="@/assets/styles/app.scss"></style>

<style lang="scss">

  // .icons_star_wars {
  //     width: 25%;
  //     margin-bottom: 3rem;
  // }

</style>
