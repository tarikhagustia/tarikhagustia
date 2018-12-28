<template>
  <section class="about-section section">
    <div class="container">
      <div class="row">
        <div class="col-sm-12 col-md-3">
          <div class="heading">
            <h3><b>About me</b></h3>
            <h6 class="font-lite-black"><b>PROFESSIONAL PATH</b></h6>
          </div>
        </div><!-- col-sm-3 -->
        <div class="col-sm-12 col-md-9">
          <p class="margin-b-50">
            Just a programmer, i'm cool enough in Web Developer using PHP as Core Language (for now), Linux users (Debian no centos :3 ), JavaScript Player (im new in JavaScript frameworks like Node and Vue) and like the future of technologies.
            so if you need a Programmer that can make your apps with the latest technologies, call me now !</p>

          <div class="row">
            <div class="col-sm-6 col-md-6 col-lg-3">
              <div class="radial-prog-area margin-b-30">
                <div class="radial-progress" data-prog-percent=".98">
                  <div></div>
                  <h6 class="progress-title">PHP</h6>
                </div>
              </div><!-- radial-prog-area-->
            </div><!-- col-sm-6-->
            <div class="col-sm-6 col-md-6 col-lg-3">
              <div class="radial-prog-area margin-b-50">
                <div class="radial-progress" data-prog-percent=".96">
                  <div></div>
                  <h6 class="progress-title">Laravel</h6>
                </div>
              </div><!-- radial-prog-area-->
            </div><!-- col-sm-6-->
            <div class="col-sm-6 col-md-6 col-lg-3">
              <div class="radial-prog-area margin-b-50">
                <div class="radial-progress" data-prog-percent=".90">
                  <div></div>
                  <h6 class="progress-title">CodeIgniter</h6>
                </div>
              </div><!-- radial-prog-area-->
            </div><!-- col-sm-6-->

            <div class="col-sm-6 col-md-6 col-lg-3">
              <div class="radial-prog-area margin-b-50">
                <div class="radial-progress" data-prog-percent=".80">
                  <div></div>
                  <h6 class="progress-title">Metatarder 4 API</h6>
                </div>
              </div><!-- radial-prog-area-->
            </div><!-- col-sm-6-->
            <div class="col-sm-6 col-md-6 col-lg-3">
              <div class="radial-prog-area margin-b-30">
                <div class="radial-progress" data-prog-percent=".70">
                  <div></div>
                  <h6 class="progress-title">VUE JS</h6>
                </div>
              </div><!-- radial-prog-area-->
            </div><!-- col-sm-6-->
            <div class="col-sm-6 col-md-6 col-lg-3">
              <div class="radial-prog-area margin-b-30">
                <div class="radial-progress" data-prog-percent=".60">
                  <div></div>
                  <h6 class="progress-title">PYTHON</h6>
                </div>
              </div><!-- radial-prog-area-->
            </div><!-- col-sm-6-->
            <div class="col-sm-6 col-md-6 col-lg-3">
              <div class="radial-prog-area margin-b-50">
                <div class="radial-progress" data-prog-percent=".50">
                  <div></div>
                  <h6 class="progress-title">REACT NATIVE</h6>
                </div>
              </div><!-- radial-prog-area-->
            </div><!-- col-sm-6-->
            <div class="col-sm-6 col-md-6 col-lg-3">
              <div class="radial-prog-area margin-b-50">
                <div class="radial-progress" data-prog-percent=".20">
                  <div></div>
                  <h6 class="progress-title">FLUTTER</h6>
                </div>
              </div><!-- radial-prog-area-->
            </div><!-- col-sm-6-->
          </div><!-- row -->
        </div><!-- col-sm-9 -->
      </div><!-- row -->
    </div><!-- container -->
  </section><!-- about-section -->
</template>

<script>
export default {
  name : 'Skill',
  mounted(){
    $(".radial-progress").each(function(){
  		var $this = $(this),
  			progPercent = $this.data('prog-percent');

  		var bar = new ProgressBar.Circle(this, {
  			color: '#aaa',
  			strokeWidth: 3,
  			trailWidth: 1,
  			easing: 'easeInOut',
  			duration: 1400,
  			text: {

  			},
  			from: { color: '#aaa', width: 1 },
  			to: { color: '#FEAE01', width: 3 },
  			// Set default step function for all animate calls
  			step: function(state, circle) {
  				circle.path.setAttribute('stroke', state.color);
  				circle.path.setAttribute('stroke-width', state.width);

  				var value = Math.round(circle.value() * 100);
  				if (value === 0) {
  					circle.setText('');
  				} else {
  					circle.setText(value);
  				}

  			}
  		});

  		$(this).waypoint(function(){
  		   bar.animate(progPercent);
  		},{offset: "90%"})

  	});
  }
}
</script>

<style lang="css">
</style>
