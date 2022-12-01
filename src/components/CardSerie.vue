<template>
    <div class="cards">
      <div class="card_img">
        <img :src="src + card.poster_path" alt="" />
      </div>
    </div>
  </template>

<script>
export default {
  name: 'CardSerie',
  props: {
    card: Object,
  },
  data() {
    return {
      src: 'https://image.tmdb.org/t/p/w342',
    };
  },
};
</script>
  <style lang="scss" scoped>
  .card_img{
      width: calc((1000px - 3rem )/ 4);
      img{
          width: 100%;
      }
  }
  </style>
