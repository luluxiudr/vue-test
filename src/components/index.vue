<template>
	<div id='index'>
		<div v-show="isBottom">
			<div class='bigdiv'>
				<div class='Special'>
					专栏
				</div>
				<div class='look_all'>
					查看全部
				</div>
			</div>
		</div>

		<div class="contentDiv" v-for="content in contents">
			<router-link :to="{path:'/list',query:{id:content.id}}">
				<img class='content_left' v-bind:src="content.src" />
				<div class='content_right'>
					<h4>{{content.title}}</h4>
					<p>{{content.work}}</p>
					<div class='bottom_icon'><span>{{content.people}}</span></div>
				</div>
			</router-link>
		</div>
  
	</div>
</template>

<script>
	export default {
		name: 'index',
		data() {
			return {
				back: false,
				transitionName: '',
				isBottom: true,
				contents: [{
						'id': 1,
						'src': "https://ss0.bdstatic.com/94oJfD_bAAcT8t7mm9GUKT-xh_/timg?image&quality=100&size=b4000_4000&sec=1536653464&di=10d97cc5c953c914cc11f2c2ff093268&src=http://img.laozu.com/ueditor/20180716/laozu5b4bf872f3ad3.jpg",
						'title': '标题1',
						'work': '内容1',
						'people': '101'
					},
					{
						'id': 2,
						'src': "https://ss0.bdstatic.com/94oJfD_bAAcT8t7mm9GUKT-xh_/timg?image&quality=100&size=b4000_4000&sec=1536653464&di=10d97cc5c953c914cc11f2c2ff093268&src=http://img.laozu.com/ueditor/20180716/laozu5b4bf872f3ad3.jpg",
						'title': '标题2',
						'work': '内容2',
						'people': '102'
					},
					{
						'id': 3,
						'src': "https://ss0.bdstatic.com/94oJfD_bAAcT8t7mm9GUKT-xh_/timg?image&quality=100&size=b4000_4000&sec=1536653464&di=10d97cc5c953c914cc11f2c2ff093268&src=http://img.laozu.com/ueditor/20180716/laozu5b4bf872f3ad3.jpg",
						'title': '标题3',
						'work': '内容3',
						'people': '103'
					},
				]
			}
		},
		methods: {

		},
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	h1,
	h2 {
		font-weight: normal;
	}
	
	ul {
		list-style-type: none;
		padding: 0;
	}
	
	li {
		display: inline-block;
		margin: 0 10px;
	}
	
	a {
		color: #42b983;
	}
</style>