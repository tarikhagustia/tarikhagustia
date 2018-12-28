<template>
  <section class="portfolio-section section">
    <div class="container">
      <div class="row">
        <div class="col-sm-12 col-md-3">
          <div class="heading">
            <h3><b>Portfolio</b></h3>
            <h6 class="font-lite-black"><b>MY WORK</b></h6>
          </div>
        </div><!-- col-sm-3 -->

        <div class="col-sm-12 col-md-9">
          <div class="portfolioFilter clearfix margin-b-80">
            <a href="#" data-filter="*" class="current"><b>ALL</b></a>
            <a href="#" data-filter=".web-design"><b>WEB APPLICATION</b></a>
          </div><!-- portfolioFilter -->
        </div><!-- col-sm-8 -->
      </div><!-- row -->

      <div class="portfolioContainer  margin-b-50">

        <div class="p-item web-design" v-for="project in projects">
          <a target="_blank" :href="project.link" data-fluidbox>
            <img :src="project.image" alt=""></a>
        </div><!-- p-item -->

      </div><!-- portfolioContainer -->
    </div><!-- container -->
  </section><!-- portfolio-section -->
</template>

<script>
export default {
  name : 'Portfolio',
  data(){
    return {
      projects : []
    }
  },
  mounted(){
    axios.get('/data/projects.json')
    .then((response) => {
      this.projects = response.data
    })
  }
}
</script>

<style lang="css">
</style>
