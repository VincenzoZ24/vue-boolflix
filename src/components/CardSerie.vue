<template>
    <div class="cards">
      <div class="card_img">
        <img :src="src + card.poster_path" alt="" />
      </div>
      <div class="back">
        <p>TITOLO: {{card.name}}</p>
        <p>TITOLO ORIGINALE: {{card.original_name}}</p>
        <p>LINGUA ORIGINALE: {{card.original_language}}</p>
        <p>VOTO: {{card.vote_average}}</p>
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
    width: 100%;
    img{
        width: 100%;
    }
}
.cards{
    width: calc((1000px - 3rem )/ 4);
    position: relative;
}
.back{
    padding: 1rem;
    color: white;
    position: absolute;
    top: 0;
    opacity: 0;
    width: 100%;
    height: 100%;
    p{
        margin-bottom: .5rem;
    }
}
.cards:hover .card_img{
    display: none;
}
.cards:hover .back{
    opacity: 1;
    transition: 2s;
    background-color: black;
}

  </style>
