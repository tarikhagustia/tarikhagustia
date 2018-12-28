<template>
  <section class="education-section section">
    <div class="container">
      <div class="row">
        <div class="col-sm-12 col-md-3">
          <div class="heading">
            <h3><b>Education</b></h3>
            <h6 class="font-lite-black"><b>ACADEMIC CAREER</b></h6>
          </div>
        </div><!-- col-sm-3 -->

        <div class="col-sm-12 col-md-9">

          <div class="education-wrapper">
            <div class="education margin-b-50" v-for="education in educations">
              <h4><b>{{education.grade}}</b></h4>
              <h5 class="font-yellow"><b>{{education.place}} - {{education.major}}</b></h5>
              <h6 class="font-lite-black margin-t-10">GRADUATED IN {{education.year}}</h6>
            </div><!-- education -->
          </div><!-- education-wrapper -->
        </div><!-- col-sm-9 -->
      </div><!-- row -->
    </div><!-- container -->

  </section><!-- education-section -->
</template>

<script>
export default {
  name : 'Education',
  data(){
    return {
      educations : []
    }
  },
  mounted(){
    axios.get('/data/educations.json')
    .then((response) => {
      this.educations = response.data
    })
  }
}
</script>

<style lang="css">
</style>
