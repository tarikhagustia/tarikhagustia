<template>
  <div class="radial-progress">
    <div></div>
    <h6 class="progress-title">{{skillName}}</h6>
  </div>
</template>

<script>
export default {
  props : ['percent', 'skillName'],
  name : 'SkillItem',
  mounted(){
    let progPercent = this.percent;

    let bar = new ProgressBar.Circle(this.$el, {
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
					// circle.setText('');
				} else {
					// circle.setText(value);
				}

			}
		});
    bar.animate(10);
  }
}
</script>

<style lang="css">
</style>
