<template>

	<div id='list'>
		<router-link to="/">返回</router-link>
		<div>{{ids}}</div>

		<el-tabs stretch="true" v-model="activeName" @tab-click="handleClick">
			<el-tab-pane label="详情" name="first">
				<div>{{work}}</div>
			</el-tab-pane>
			<el-tab-pane label="目录" name="second">

				<div class="contentDiv" v-for="content in contents">
					<img class='content_left' v-bind:src="content.src" />
					<div class='content_right'>
						<h4>{{content.title}}</h4>
						<p>{{content.work}}</p>
						<div class='bottom_icon'><span>{{content.people}}</span></div>
					</div>

				</div>

			</el-tab-pane>
		</el-tabs>
	</div>
</template>

<script>
	export default {
		name: 'list',
		components: {},
		data() {
			return {
				work: '',
				activeName: 'first',
				contents: [],
				ids: '',
			}
		},
		methods: {
			handleClick(tab, event) {

			}
		},
		watch: {
			'$route' (to, from) {
				this.ids = "这是第" + this.$route.query.id + "的详情页";
				this.work = "这是第" + this.ids + "的富文本内容";
				this.contents = Object.assign({}, this.contents, [{
						'id': 1,
						'src': "https://ss0.bdstatic.com/94oJfD_bAAcT8t7mm9GUKT-xh_/timg?image&quality=100&size=b4000_4000&sec=1536653464&di=10d97cc5c953c914cc11f2c2ff093268&src=http://img.laozu.com/ueditor/20180716/laozu5b4bf872f3ad3.jpg",
						'title': this.ids,
						'work': '内容1',
						'people': '100'
					},
					{
						'id': 2,
						'src': "https://ss0.bdstatic.com/94oJfD_bAAcT8t7mm9GUKT-xh_/timg?image&quality=100&size=b4000_4000&sec=1536653464&di=10d97cc5c953c914cc11f2c2ff093268&src=http://img.laozu.com/ueditor/20180716/laozu5b4bf872f3ad3.jpg",
						'title': this.ids,
						'work': '内容1',
						'people': '100'
					},
					{
						'id': 3,
						'src': "https://ss0.bdstatic.com/94oJfD_bAAcT8t7mm9GUKT-xh_/timg?image&quality=100&size=b4000_4000&sec=1536653464&di=10d97cc5c953c914cc11f2c2ff093268&src=http://img.laozu.com/ueditor/20180716/laozu5b4bf872f3ad3.jpg",
						'title': this.ids,
						'work': '内容1',
						'people': '100'
					},
				])

			}

		},
		created() {
			let ids = this.$route.query.id;
			this.ids = '这是第' + ids + '的详情页';
			this.work = "这是第" + this.ids + "的富文本内容";
							this.contents = Object.assign({}, this.contents, [{
						'id': 1,
						'src': "https://ss0.bdstatic.com/94oJfD_bAAcT8t7mm9GUKT-xh_/timg?image&quality=100&size=b4000_4000&sec=1536653464&di=10d97cc5c953c914cc11f2c2ff093268&src=http://img.laozu.com/ueditor/20180716/laozu5b4bf872f3ad3.jpg",
						'title': this.ids,
						'work': '内容1',
						'people': '100'
					},
					{
						'id': 2,
						'src': "https://ss0.bdstatic.com/94oJfD_bAAcT8t7mm9GUKT-xh_/timg?image&quality=100&size=b4000_4000&sec=1536653464&di=10d97cc5c953c914cc11f2c2ff093268&src=http://img.laozu.com/ueditor/20180716/laozu5b4bf872f3ad3.jpg",
						'title': this.ids,
						'work': '内容1',
						'people': '100'
					},
					{
						'id': 3,
						'src': "https://ss0.bdstatic.com/94oJfD_bAAcT8t7mm9GUKT-xh_/timg?image&quality=100&size=b4000_4000&sec=1536653464&di=10d97cc5c953c914cc11f2c2ff093268&src=http://img.laozu.com/ueditor/20180716/laozu5b4bf872f3ad3.jpg",
						'title': this.ids,
						'work': '内容1',
						'people': '100'
					},
				])
		}
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