<template>
	<div class='content'>
		<div class='banner'>
			<h1>智慧城市大计划</h1>
			<img :src='src' />
		</div>
		<div class='introduce'>
			<div class='pic mar1'>
				<img :src='src2' />
				<div class='ad'>
					<h3>智能交通系统</h3>
					<p class='word'>道路收费系统</p>
					<p class='word'>多功能智能交通卡系统</p>
					<p class='word'>数字化交通智能信息管理系统</p>
				</div>
			</div>
			<div class='pic mar1'>
				<img :src='src3' />
				<div class='ad'>
					<h3>智慧能源系统</h3>
					<p class='word'>传感测量技术</p>
					<p class='word'>通讯技术</p>
					<p class='word'>计算机技术</p>
					<p class='word'>控制技术与清洁能源</p>
				</div>
			</div>
			<div class='pic mar1'>
				<img :src='src4' />
				<div class='ad'>
					<h3>智能物流及建筑服务系统</h3>
					<p class='word'>基于位置的物流技术</p>
					<p class='word'>物物之间的信息交换、共享</p>
					<p class='word'>物流各环节的实时跟踪和监控</p>
					<p class='word'>现代的网络技术</p>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
	export default {
		name: 'shareContent',
		data () {
			return {
				src: '/static/img/share1.jpg',
				src2: '/static/img/share2.jpg',
				src3: '/static/img/share3.jpg',
				src4: '/static/img/share4.jpg',
			}
		}
	}
</script>
<style lang='scss'>
	@mixin fade-in {
        -webkit-animation: fadeIn 2s 0.5s ease both;
        -moz-animation: fadeIn 2s 0.5s ease both;
        -ms-animation: fadeIn 2s 0.5s ease both;
        -o-animation: fadeIn 2s 0.5s ease both;
        animation: fadeIn 2s 0.5s ease both;		
	}
	.content .banner h1{
		position: absolute;
		width: 100%;
		top: 40%;
		z-index: 8;
		color: white;
		font-size: 66px;
		@include fade-in;
	}
	.introduce {
		position: relative;
		width: 100%;
		height: 100%;
		top: -10%;
		img {
			width: 500px;
			height: 400px;
		}
	}
	.pic{
		position: relative;
		img{
			left: -15%;
			position: relative;
		}
	}	
	.ad{
		position: absolute;
		top: 10%;
		left: 55%;
        width: 336px;
		 h3 {
			text-align: left;
			font-size: 36px;
			color: #585858;
			font-weight: 500;
		}
	}
	.word{
		font-size: 14px;
		color: #4b4b4b;
		line-height: 22px;
		text-align: left;
		margin: 0;
		padding: 0;
        padding-bottom: 10px;
	}
	.mar1{
		margin: 50px 0 50px;
	}
</style>