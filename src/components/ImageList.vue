<template>
  <div>
    <div class="container image-detail">
      <div class="row">
        <div class="col-sm-8 col-xs-12">
          <img :src="selectedImage.imageLink" class="img-responsive">
        </div>
        <div class="col-sm-4 col-xs-12">
          <h1>{{selectedImage.title}}</h1>
          <p>{{selectedImage.description}}</p>
        </div>
      </div>
    </div>
    <a @click="showImage(image)" v-for="image in images" v-bind:key="image.id" href="#"><div class="col-md-3 col-sm-4 col-xs-6"><img class="img-responsive" :src="image.thumbnail" /></div></a>
  </div>
</template>

<script>
export default {
  props: ['images'],
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
