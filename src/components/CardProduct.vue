<script>
export default {
  props: {
    movie: Object,
  },
};
</script>

<template>
  <div class="card">
    <img :src="movie.thumb" alt="img" />
    <h3>{{ movie.series }}</h3>
  </div>
</template>

<style lang="scss" scoped>
.card {
  width: 16%;
  gap: 3%;
  img {
    width: 100%;
  }
  h3 {
    color: white;
    margin-top: 1rem;
  }
}
</style>
