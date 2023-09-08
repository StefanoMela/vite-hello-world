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
  <div class="container d-flex justify-content-center overlay-content">
    <img :src="buildImagePath(image)" alt="" class="overlay-lighten">
    <p class="display-3 overlay-text">Jumbotron</p>
  </div>
</template>

<style scoped>

img {

  max-width: 750px;

};

.overlay-content {
  text-align: center;
  position: relative;
}

.overlay-lighten {
  opacity: 0.6;
  }
  
.overlay-darken {
filter: brightness(50%);
  }

.overlay-text {
  position: absolute;
  top: 40%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>
