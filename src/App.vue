<template>
  <div id="app">
  	<app-header v-bind:info="info" v-on:infoChanged="updateInfo($event)"></app-header>
  	<users v-bind:users="users"></users>
  	<app-footer v-bind:info="info"></app-footer>
  </div>
</template>

<script>

//局部注册组件
import Users from './components/Users'
import Header from './components/Header'
import Footer from './components/Footer'

export default {
  name: 'App',
  data(){
  	return {
  		title: "这是一个CLI项目！",
  		users:[
				{name:"Henry",position:"web开发",show:false},
				{name:"Bucky",position:"web开发",show:false},
				{name:"Emily",position:"web开发",show:false},
				{name:"Emily",position:"web开发",show:false},
				{name:"Emily",position:"web开发",show:false},
				{name:"Emily",position:"web开发",show:false},
				{name:"Emily",position:"web开发",show:false}
			],
			info:"这是传值！String Boolean Null Number"
  	}
  },
  methods:{
  	updateInfo: function (info) {
  		this.info = info
  	}
  },
  components:{Users,"app-header": Header,"app-footer":Footer}
}
</script>

<style scoped>
</style>
