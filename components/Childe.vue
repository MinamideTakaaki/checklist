<template>
	<div class="child">
		{{ user.name[0] }} <br>
		{{ user.name[1] }} <br>
		{{ user.age }}
	</div>
</template>

<script>
import Vue from 'vue'

export default Vue.extend({
	props: ['user']
})
</script>