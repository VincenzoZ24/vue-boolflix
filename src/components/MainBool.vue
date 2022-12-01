<template>
  <main v-if="(arrMovieName.length != 0)">
    <h1>FILM</h1>

    <div class="container">

      <CardFilm
        class="content"
        v-for="card in arrMovieName"
        :key="card.poster_path"
        :card="card"
      />

    </div>
    <h1>SERIE</h1>
    <div class="container">
        <CardSerie class=" content"
        v-for="card in arrSerieName"
        :key="card.poster_path"
        :card="card"/>
    </div>

  </main>
</template>

<script>
import CardFilm from '@/components/CardFilm.vue';
import CardSerie from '@/components/CardSerie.vue';

export default {
  name: 'MainBool',

  props: {
    arrMovieName: Array,
    arrSerieName: Array,
  },
  components: {
    CardFilm,
    CardSerie,
  },
};
</script>

<style lang="scss" scoped>
main {
  background-color: gray;
}
.container{
  display: flex;
  flex-wrap: wrap;
  max-width: 1000px;
  gap: 1rem;

  margin: auto;
  margin-top: 4rem;
  padding-bottom: 4rem;
}
h1{
    padding: 1rem;
}
</style>
