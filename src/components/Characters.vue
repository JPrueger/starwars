<template>

  <div>

     <div class="c" v-for="character in list" v-bind:key="character.name">
        <h2>Name: {{ character.name }}</h2>
        <p>{{ character.height }}</p>
        <p>{{ character.mass }}</p>
        <p>{{ character.hair_color }}</p>
        <p>{{ character.skin_color }}</p>
        <p>{{ character.birth_year }}</p>
        <p>{{ character.gender }}</p>
      </div>

  </div>

</template>

<script>

import Vue from 'vue'
import Axios from 'axios'
import VueAxios from 'vue-axios'

Vue.use(VueAxios, Axios)

export default {
    name: "Characters",

    data () {
        return {list:undefined}
    },

    mounted () {
        Vue.axios.get('https://swapi.dev/api/people/')
        .then((response) => {
            this.list=response.data.results
            // console.warn(response.results)
            console.log(response.data.results)
        })
    }
}

</script>


<style lang="scss">

 @import '@/assets/styles/variables.scss';


</style>
