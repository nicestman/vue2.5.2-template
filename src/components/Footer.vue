<template>
	<header>
		<p>{{copyright}} {{info}}</p>
	</header>
</template>

<script>
	export default {
		name: 'app-footer',
		props:{
			info:{
				type:String
			}
		},
		data() {
			return {
				copyright: "Copyright 2017 Vue Demo"
			}
		}
	}
</script>

<style scoped>
	header{
		background: #222;
		padding: 6px;
	}
	p{
		color: lightgreen;
		text-align: center;
	}
</style>