<template>
  <div class="cards" >
    <div class="card_img">
      <img :src="src + card.poster_path" alt="" />
    </div>
    <div class="back">
        <p>TITOLO: {{card.title}}</p>
        <p>TITOLO ORIGINALE: {{card.original_title}}</p>
        <p>LINGUA ORIGINALE: {{card.original_language}}</p>
        <p>VOTO: {{card.vote_average}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardFilm',
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
    transform: rotate(0deg);
    backface-visibility: hidden;
    transition: transform 0.4s linear;
    img{
        width: 100%;
    }
}
.cards{
    width: calc((1000px - 3rem )/ 4);
    position: relative;
    perspective: 1000px;
}
.back{
    padding: 1rem;
    color: white;
    position: absolute;
    top: 0;

    width: 100%;
    height: 100%;
    transform: rotateY(180deg);
    backface-visibility: hidden;
    transition: transform 0.4s linear;
    p{
        margin-bottom: .5rem;
    }
}
.cards:hover .card_img{
    transform: rotateY(-180deg);
}
.cards:hover .back{
    transform: rotateY(0deg);
    transition: 2s;
    background-color: black;
}

</style>
