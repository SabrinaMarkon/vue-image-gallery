<template>
  <div>
    <single-image :selectedImage="selectedImage"></single-image>
    <a @click="showImage(image)" v-for="image in images" v-bind:key="image.id" href="#"><div class="col-md-3 col-sm-4 col-xs-6"><img class="img-responsive" :src="image.thumbnail" /></div></a>
  </div>
</template>

<script>
import SingleImage from './SingleImage'

export default {
  props: ['images'],
  components: {SingleImage},
  data () {
    return {
      selectedImage: ''
    }
  },
  // In Vue, we can define a method in a component by using the methods option. We can add the methods option right below the data option
  methods: {
    showImage: function (image) {
      this.selectedImage = image
    }
  }
}
</script>
