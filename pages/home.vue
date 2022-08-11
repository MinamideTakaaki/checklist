<template>
	<div class="parent">
		<Childe :user="user" />
	</div>
</template>

<script>
import Vue from 'vue';
import axios from 'axios';
import Childe from '~/components/Childe.vue';

export default {
	components: {
		Childe
	},
	data() {
		return {
			user: [
				{
					"name": [],
					"age": ""
				}
			]
		}
	},
	created: function () {
		axios.get('list_data.json')
			.then(response => {
				let json = response.data;
				this.user = json;
			})
			.catch(err =>{
				console.error(err)
			})
	}
}

</script>