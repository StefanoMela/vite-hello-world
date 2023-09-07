<script>
export default {
  data() {
    return {

      image: '../assets/img/haotian-zheng-Dr7TUl4BURo-unsplash.jpg'
    };
  },

  methods: {

    buildImagePath (path) {

      const imageUrl = new URL('../assets/img/haotian-zheng-Dr7TUl4BURo-unsplash.jpg', import.meta.url);

      return imageUrl.href

    },
  }
};
</script>

<template>
  <div class="container d-flex justify-content-center">
    <img :src="buildImagePath(image)" alt="">
  </div>
</template>

<style scoped>

img {

  max-width: 750px;

};
</style>
