<template>
  <div class="gallery">
    <div class="container">
      <div class="row">
        <a href="#">
          <div class="col-md-3 col-sm-4 col-xs-6"><img class="img-responsive" src="https://vuejsbook.com/img/vuejs/img1.jpg" /></div>
        </a>
        <a href="#">
          <div class="col-md-3 col-sm-4 col-xs-6"><img class="img-responsive" src="https://vuejsbook.com/img/vuejs/img2.jpg" /></div>
        </a>
        <a href="#">
          <div class="col-md-3 col-sm-4 col-xs-6"><img class="img-responsive" src="https://vuejsbook.com/img/vuejs/img3.jpg" /></div>
        </a>
        <a href="#">
          <div class="col-md-3 col-sm-4 col-xs-6"><img class="img-responsive" src="https://vuejsbook.com/img/vuejs/img4.jpg" /></div>
        </a>
        <a href="#">
          <div class="col-md-3 col-sm-4 col-xs-6"><img class="img-responsive" src="https://vuejsbook.com/img/vuejs/img5.jpg" /></div>
        </a>
        <a href="#">
          <div class="col-md-3 col-sm-4 col-xs-6"><img class="img-responsive" src="https://vuejsbook.com/img/vuejs/img6.jpg" /></div>
        </a>
        <a href="#">
          <div class="col-md-3 col-sm-4 col-xs-6"><img class="img-responsive" src="https://vuejsbook.com/img/vuejs/img7.jpg" /></div>
        </a>
        <a href="#">
          <div class="col-md-3 col-sm-4 col-xs-6"><img class="img-responsive" src="https://vuejsbook.com/img/vuejs/img8.jpg" /></div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      message: 'This is a gallery component'
    }
  }
}
</script>

<style scoped>
  img {
    -webkit-box-shadow: 0px 1px 6px 1px rgba(0,0,0,0,0.75);
    -moz-box-shadow: 0px 1px 6px 1px rgba(0,0,0,0,0.75);
    box-shadow: 0px 1px 6px 1px rgba(0,0,0,0,0.75);
    margin-bottom: 20px;
  }
  img:hover {
    filter: gray; /* IE6-9 */
    -webkit-filter: grayscale(1); /* Google Chrome, Safari 6+ & Opera 15+ */
  }
</style>
