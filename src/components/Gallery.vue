<template>
  <div class="gallery">
    <a v-for="image in images" v-bind:key="image.id" href="#">
      <div class="col-md-3 col-sm-4 col-xs-6"><img class="img-responsive" v-bind:src="image.thumbnail" /></div>
    </a>
  </div>
</template>

<script>
/*
** Please remember that: "If we want to display any image (loaded from our data) in Vue, we must use :src or v-bind:src"

v-if - used to conditionally display or hide an element. If the condition is true, it will render the element.

v-else - works just like v-if, but the condition is false.

v-show - can be used instead of v-if. However, v-show always compiles and renders everything, and it just uses display:none (a CSS property) to hide the element.

v-on - used to attach an event listener to an element.

v-for - used to render a list of items.
*/

export default {
  data () {
    return {
      images: [
        { id: 0, thumbnail: 'https://vuejsbook.com/img/vuejs/img1.jpg' },
        { id: 1, thumbnail: 'https://vuejsbook.com/img/vuejs/img2.jpg' },
        { id: 2, thumbnail: 'https://vuejsbook.com/img/vuejs/img3.jpg' },
        { id: 3, thumbnail: 'https://vuejsbook.com/img/vuejs/img4.jpg' },
        { id: 4, thumbnail: 'https://vuejsbook.com/img/vuejs/img5.jpg' },
        { id: 5, thumbnail: 'https://vuejsbook.com/img/vuejs/img6.jpg' },
        { id: 6, thumbnail: 'https://vuejsbook.com/img/vuejs/img7.jpg' },
        { id: 7, thumbnail: 'https://vuejsbook.com/img/vuejs/img8.jpg' }
      ]
    }
  }
}
</script>

<style scoped>
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
