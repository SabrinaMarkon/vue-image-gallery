<template>
  <div class="gallery">
    <div class="container">
      <div class="row">
        <single-image :selectedImage="selectedImage"></single-image>
        <image-list :images="images" v-on:emitImage="showImage"></image-list>
      </div>
    </div>
  </div>
</template>

<script>
import ImageList from './ImageList'
import SingleImage from './SingleImage'
/*
** Please remember that: "If we want to display any image (loaded from our data) in Vue, we must use :src or v-bind:src"

v-if - used to conditionally display or hide an element. If the condition is true, it will render the element.

v-else - works just like v-if, but the condition is false.

v-show - can be used instead of v-if. However, v-show always compiles and renders everything, and it just uses display:none (a CSS property) to hide the element.

v-on - used to attach an event listener to an element. Short form: ie. @click is short for v-on:click.

v-for - used to render a list of items.
*/

export default {
  name: 'gallery',
  components: {SingleImage, ImageList},
  data () {
    return {
      selectedImage: '',
      images: [
        { id: 1, title: 'First image', description: 'First image description', thumbnail: 'https://vuejsbook.com/img/vuejs/img1.jpg', imageLink: 'https://vuejsbook.com/img/vuejs/img1-l.jpg' },
        { id: 2, title: 'Second image', description: 'Second image description', thumbnail: 'https://vuejsbook.com/img/vuejs/img2.jpg', imageLink: 'https://vuejsbook.com/img/vuejs/img2-l.jpg' },
        { id: 3, title: 'Third image', description: 'Third image description', thumbnail: 'https://vuejsbook.com/img/vuejs/img3.jpg', imageLink: 'https://vuejsbook.com/img/vuejs/img3-l.jpg' },
        { id: 4, title: 'Fourth image', description: 'Fourth image description', thumbnail: 'https://vuejsbook.com/img/vuejs/img4.jpg', imageLink: 'https://vuejsbook.com/img/vuejs/img4-l.jpg' },
        { id: 5, title: 'Fifth image', description: 'Fifth image description', thumbnail: 'https://vuejsbook.com/img/vuejs/img5.jpg', imageLink: 'https://vuejsbook.com/img/vuejs/img5-l.jpg' },
        { id: 6, title: 'Sixth image', description: 'Sixth image description', thumbnail: 'https://vuejsbook.com/img/vuejs/img6.jpg', imageLink: 'https://vuejsbook.com/img/vuejs/img6-l.jpg' },
        { id: 7, title: 'Seventh image', description: 'Seventh image description', thumbnail: 'https://vuejsbook.com/img/vuejs/img7.jpg', imageLink: 'https://vuejsbook.com/img/vuejs/img7-l.jpg' },
        { id: 8, title: 'Eight image', description: 'Eighth image description', thumbnail: 'https://vuejsbook.com/img/vuejs/img8.jpg', imageLink: 'https://vuejsbook.com/img/vuejs/img8-l.jpg' }
      ]
    }
  },
  methods: {
    showImage: function(image) {
      this.selectedImage = image
    }
  }
}
</script>

<style>
img {
  -webkit-box-shadow: 0px 1px 6px 1px rgba(0, 0, 0, 0, 0.75);
  -moz-box-shadow: 0px 1px 6px 1px rgba(0, 0, 0, 0, 0.75);
  box-shadow: 0px 1px 6px 1px rgba(0, 0, 0, 0, 0.75);
  margin-bottom: 20px;
}
img:hover {
  filter: gray; /* IE6-9 */
  -webkit-filter: grayscale(1); /* Google Chrome, Safari 6+ & Opera 15+ */
}
</style>
