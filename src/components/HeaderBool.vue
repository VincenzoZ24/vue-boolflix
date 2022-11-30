<template>
  <div class="nav_boolflix">
    <h1>BOOLFLIX</h1>
    <div class="right_nav">
        <label for="get">
        <input type="text" v-model="cerca">
    </label>
    <button @click="generaCards">CERCA</button>
    </div>

  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'HeaderBool',
  data() {
    return {
      cerca: '',
      arrMovies: [],
    };
  },
  methods: {
    generaCards() {
      axios.get(`https://api.themoviedb.org/3/search/movie?api_key=eddeb9cc139fc5540af4fe0bcd294c59&language=it-IT&query=${this.cerca}`)
        .then((axiosResponse) => {
          this.arrMovies = axiosResponse.data.results;
          this.$emit('movie-received', this.arrMovies);
        });
    },

  },
};
</script>

<style lang="scss" scoped>
.nav_boolflix{
    display: flex;
    padding: 1rem;
    justify-content: space-between;
    align-items: center;
    height: 4rem;
    background-color: black;
    h1{
        color: red;
    }
}
.right_nav{
    input{
        margin-right: 1rem;
        padding: .5rem;
        border: none;
        border-radius: 1rem;
    }
    button{
        padding: .5rem;
        border: none;
        border-radius: 1rem;
        cursor: pointer;
    }
}
</style>
