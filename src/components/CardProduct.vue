<script>
export default {
  props: {
    movie: Object,
  },
};
</script>

<template>
  <div class="card">
    <div class="card-img">
      <img :src="movie.thumb" alt="img" />
    </div>
    <div class="card-text">
      <h3>{{ movie.series }}</h3>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  width: calc(100% / 7);
  max-height: 250px;
  margin-bottom: 1%;
  cursor: pointer;

  .card-img {
    width: 100%;
    aspect-ratio: 1;

    img {
      width: 100%;
      height: 100%;
    }
  }
  .card-text {
    width: 100%;
    height: 2.5rem;
  }

  h3 {
    color: white;
    margin-top: 1rem;
    font-size: 1rem;
  }
}
</style>
