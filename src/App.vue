<template>
  <div id="app">
    <div class="container">
      <!-- <div class="card shadow-lg"> -->
        <!-- <div class="card-body"> -->
          <test-action
            v-for="(action, index) in actions"
            v-bind:name="action.name"
            v-bind:steps="action.steps"
            v-bind:key="index"
	        ></test-action>
    <!-- </div> -->
  <!-- </div> -->
  </div>
  </div>
</template>

<script>
import TestAction from "./components/TestAction"

export default {
  name: 'app',
  components: {
    TestAction
  },


  data: function(){
    return {
      actions: [
				{
					"name": "Action1",
					"steps": 
						[
							{
							"name" : "step1",
							"level": "<div>aewfsefs</div>",
							"time": "time"
							},
							
							{
							"name" : "step2",
							"level": "error",
							"time": "time"
							}
						] 
					
				
				},
				
				{
					"name": "Action2",
					"steps": 
						[
							{
							"name" : "step3",
							"level": "info",
							"time": "time"
							},
							
							{
							"name" : "step4",
							"level": "error",
							"time": "time"
							}
					] 
				}
	] 



    }
    
  } 
}
</script>

<style>
 #app {
  /* font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50; */
  /* background: rgba(0, 0, 0, 0.6); */
  
  margin-top: 60px;
}

body {
    background: #37474f !important;
}


</style>
