<template>

	<div class="test-action">
		<div class="action-header">
			<button class="btn btn-primary btn-sm" @click="expandCollapse">
				<span v-show="!expanded"><i class="fa fa-plus"></i></span>
				<span v-show="expanded"><i class="fa fa-minus"></i></span>
				
			</button>
			<span class="action-name">{{name}}</span>
		</div>
		
		<div class="steps" v-show="expanded == true">
			<test-step
				v-for="(step, index) in steps"
				v-bind:name="step.name"
				v-bind:time="step.time"
				v-bind:level="step.level"

				v-bind:key="index"
			></test-step>
		</div>
	</div>
		
</template>

<script>
import TestStep from './TestStep'
export default {
  name: "TestAction",
  props: ["name", "steps"],
  components: {TestStep},

  data: function() {
    return {
		expanded: false,
		buttonClass: 'fa fa-plus'
	};
  },

  methods: {
	expandCollapse: function(){
		  this.expanded = !this.expanded;
		  this.buttonClass = (this.expanded ? 'fa fa-minus' : 'fa fa-plus')

	  }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.test-action {
	/* background-color: #a6cbd8; */
	background: #f5f5f7;
	box-shadow: 0 0 15px rgba(0,0,0,0.3);
	margin: 20px 20px;
	 border: 1px solid grey;
	border-radius: 4px;
}

.action-header {
	margin: 10px 5px;
	
	/* font-weight: bold */
}

.action-name {
	margin-left: 10px;
	font-weight: bold
}

.expand-action {
	/* margin-left: 10px;
	height:25px;
   	width:25px; */
}

.steps {
	margin: 10px 30px;
	
}

/* #currentProgress {
  margin-bottom: 30px;
} */
</style>
