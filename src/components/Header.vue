<template>
	<header v-on:click="changeInfo">
		<h1>{{title}} {{info}}</h1>
	</header>
</template>

<script>
	export default {
		name: 'app-header',
		props:{
			info:{
				type:String
			}
		},
		data() {
			return {
				title: "Vue.js Demo"
			}
		},
		methods:{
			changeInfo: function () {
				//this.info = "changedInfo"
				//利用$emit注册自定义事件，然后在父组件调用自定义事件，在函数传入参数$event，$event==$emit的参数二的值
				this.$emit("infoChanged","子组件向父组件传值")
			}
		}
	}
</script>

<style scoped>
	header{
		background: lightgreen;
		padding: 10px;
	}
	h1{
		color: #222;
		text-align: center;
	}
</style>