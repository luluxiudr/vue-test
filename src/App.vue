<template>

	<div id="app">

		<transition :name="transitionName">
			<keep-alive>
				<router-view></router-view>
			</keep-alive>
		</transition>
	</div>
</template>

<script>
	export default {
		name: 'App',
		components: {},
		data() {
			return {
				back: false,
				transitionName: '',
				isBottom: true,
				bottomArr: ['/index', '/list']
			}
		},
		methods: {
			change: function(event) {
				if(this.isBottom == true) {
					this.isBottom = false;
					this.back = true;
				} else {
					this.isBottom = true;
					this.back = false;
				}

			}
		},
		watch: {

		}
	}
</script>
<style rel="stylesheet/css" lang="css">
	@import "./common/css/index";
</style>