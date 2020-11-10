<template>

  <div>
    <h2>Here's a list of all Star Wars characters:</h2>
    <div class="wrapper_card">
      <div class="c" v-for="character in list" v-bind:key="character.name">
        <div class="card">
          <h3>{{ character.name }}</h3>
          <p>Height: {{ character.height }}</p>
          <p>Mass: {{ character.mass }}</p>
          <p>Hair Color: {{ character.hair_color }}</p>
          <p>Skin Color: {{ character.skin_color }}</p>
          <p>Birth Year: {{ character.birth_year }}</p>
          <p>Gender: {{ character.gender }}</p>
        </div>
      </div>
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

  .wrapper_card {
    display: grid;
    grid-column-gap: 35px;
    padding-left: 10rem;
    padding-right: 10rem;
    grid-auto-flow: row;  
    grid-template-columns: repeat(auto-fit,minmax(300px, 1fr)); 
    margin-bottom: 2rem;
  }

  .card {
    background-color: white;
    margin-bottom: 3rem;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24); 
    border-radius: 5px;
    padding: 20px 0 20px 0;
  }


</style>
