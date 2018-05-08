<template>
	<div>
		<ul>
		 	<li v-for="(car, key) in cars" :key="car.id"> 
		 	{{car.brand}} {{ car.model }} </li>
		 	
        </ul>

	</div>

</template>

<script>

import {cars} from '../services/cars'

export default {
 data () {
 	return {
 		cars: []
 	}
 },

 created () {
 	cars.getAll()
 		.then((response) => {
 			this.cars = response.data
 			console.log(this.cars)
 		}).catch((error) => {
 			console.log(error)
 		})
 }
}
	

</script>