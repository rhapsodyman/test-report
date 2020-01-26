<template>
    <div class="row step">
      <div class="col">
        <div>{{name}}</div>
    </div>
    <div class="col">
        <div>{{time}}</div>
    </div>
    <div class="col">
        <div>{{level}}</div>
    </div>
		</div>
</template>

<script>
export default {
  name: 'UserFormStep1',

  props: ["name", "time", "level"],



  data: function() {
    return {  }

 
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

.step {
  /* border: 1px solid grey; */
  margin-top: 2px;
}



</style>