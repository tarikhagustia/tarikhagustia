<template>
  <section class="experience-section section">
    <div class="container">
      <div class="row">
        <div class="col-sm-12 col-md-3">
          <div class="heading">
            <h3><b>Work Experience</b></h3>
            <h6 class="font-lite-black"><b>PREVIOUS JOBS</b></h6>
          </div>
        </div><!-- col-sm-3 -->

        <div class="col-sm-12 col-md-9">
          <div class="experience margin-b-50" v-for="experience in experiences">
            <h4><b>{{experience.possition}}</b></h4>
            <h5 class="font-yellow"><b>{{experience.place}}</b></h5>
            <h6 class="font-lite-black margin-t-10">{{experience.date}}</h6>
            <p class="margin-tb-30" v-html="experience.desc">Duis non volutpat arcu, eu mollis tellus. Sed finibus aliquam neque sit amet sodales.
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla maximus pellentes que velit,
              quis consequat nulla effi citur at. Maecenas sed massa tristique.Duis non volutpat arcu,
              eu mollis tellus. Sed finibus aliquam neque sit amet sodales. </p>
          </div><!-- experience -->
        </div><!-- col-sm-9 -->
      </div><!-- row -->
    </div><!-- container -->
  </section><!-- experience-section -->
</template>

<script>
export default {
  name : 'Experience',
  data(){
    return {
      experiences : []
    }
  },

  mounted(){
    console.log('Heee');
    axios.get('/data/experiences.json')
    .then((response) => {
      this.experiences = response.data
    })
  }
}
</script>

<style lang="css">
</style>
