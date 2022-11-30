<template>
<div id="app">
    <HeaderBool @movie-received="arrMovies = $event"/>
    <MainBool :arr-movie-name="arrMovies"/>
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
      arrMovies: null,
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
