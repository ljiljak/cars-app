<template>
<div class="">
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css" integrity="sha384-PsH8R72JQ3SOdhVi3uxftmaW6Vc51MKb0q5P2rRUpPvrszuE4W1povHYgTpBfshb" crossorigin="anonymous"> 
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">

<form>
  <div class="form-group row">
    <label for="carbrand" class="col-4 col-form-label">Brand</label> 
    <div class="col-8">
      <input v-model="car.brand" name="brand" type="text" required="required" class="form-control here">
    </div>
  </div>
  <div class="form-group row">
    <label for="carmodel" class="col-4 col-form-label">Model</label> 
    <div class="col-8">
      <input v-model="car.model" name="model" type="text" required="required" class="form-control here">
    </div>
  </div>
  <div class="form-group row">
    <label for="car.year" class="col-4 col-form-label">Year</label> 
    <div class="col-8">
      <select v-model="car.year" name="year" required="required" type="date" class="custom-select"></select>
    </div>
  </div>
  <div class="form-group row">
    <label for="car.maxSpeed" class="col-4 col-form-label">Max Speed</label> 
    <div class="col-8">
      <input v-model="car.maxSpeed" name="maxSpeed" type="number" required="required" class="form-control here">
    </div>
  </div>
  <div class="form-group row">
    <label for="car.numberOfDoors" class="col-4 col-form-label">Doors Number</label> 
    <div class="col-8">
      <input v-model="car.numberOfDoors" name="numberOfDoors" type="number" required="required" class="form-control here">
    </div>
  </div>
  <div class="form-group row">
    <label class="col-4">Autmatic Gear Box</label> 
    <div class="col-8">
      <label class="custom-control custom-checkbox">
        <input v-model="car.isAutomatic" name="isAutomatic" type="checkbox" required="required" class="custom-control-input" value="true"> 
        <span class="custom-control-indicator"></span> 
        <span class="custom-control-description">Yes</span>
      </label>
      <label class="custom-control custom-checkbox">
        <input v-model="car.isAutomatic" name="isAutomatic" type="checkbox" required="required" class="custom-control-input" value="false"> 
        <span class="custom-control-indicator"></span> 
        <span class="custom-control-description">No</span>
      </label>
    </div>
  </div>
  <div class="form-group row">
    <label class="col-4">Engine</label> 
    <div class="col-8">
      <label class="custom-control custom-radio">
        <input v-model="car.engine" name="engine" type="radio" required="required" class="custom-control-input" value="diesel"> 
        <span class="custom-control-indicator"></span> 
        <span class="custom-control-description">Diesel</span>
      </label>
      <label class="custom-control custom-radio">
        <input v-model="car.engine" name="engine" type="radio" required="required" class="custom-control-input" value="petrol"> 
        <span class="custom-control-indicator"></span> 
        <span class="custom-control-description">Petrol</span>
      </label>
      <label class="custom-control custom-radio">
        <input v-model="car.engine" name="engine" type="radio" required="required" class="custom-control-input" value="electric"> 
        <span class="custom-control-indicator"></span> 
        <span class="custom-control-description">Electric</span>
      </label>
      <label class="custom-control custom-radio">
        <input v-model="car.engine" name="car.engine" type="radio" required="required" class="custom-control-input" value="hybrid"> 
        <span class="custom-control-indicator"></span> 
        <span class="custom-control-description">Hybrid</span>
      </label>
    </div>
  </div> 
  <div class="form-group row">
    <div class="offset-4 col-8">
      <button name="submit" type="submit" class="btn btn-primary">Submit</button>
    </div>
  </div>
</form>
</div>
</template>

<script>

export default {
	data () {
		return {
			car: {
				brand: '',
				model: '',
				year: 0,
				maxSpeed: '',
				numberOfDoors: '',
				isAutomatic: false,
				engine: ''
			}
		}
	},
	computed: {
		year () {
			for ( y = 1990; y <= 2018; y++) {
				return this.y
			}
		}
	},
 }


</script>