<template>
<div id="app">
    <HeaderBool @movie-received="arrMovies = $event"
    @serie-received="arrSerie = $event" />
    <MainBool :arr-movie-name="arrMovies" :arr-seie-name="arrSerie"/>
</div>
</template>

<script>
import MainBool from '@/components/MainBool.vue';
import HeaderBool from '@/components/HeaderBool.vue';

export default {
  name: 'App',
  components: {
    HeaderBool,
    MainBool,
  },
  data() {
    return {
      arrMovies: [],
      arrSerie: [],
    };
  },
};
</script>

<style lang="scss">
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

</style>
