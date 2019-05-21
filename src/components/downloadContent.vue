<template>
	<div class='content'>
		<div class='banner'>
			<h3 id='download'>物联世界</h3>
			<p>打造全新的智慧城市</p>
			<img :src='src' />
		</div>
		<div class='teach'>
			<h3>核心产品</h3>
			<div class='step'>
				<div class='container' v-for='item in docs'>
					<img :src='item.src' />
					<h3 v-html='item.h3'></h3>
					<p v-html='item.p'></p>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
	const docs = [{
		src: '/static/img/steps1.jpg',
		h3: '<em>①</em>智慧物联综合管理平台',
		p: '智慧物联综合管理平台以海量多源异构物联网设备为载体，支持亿万量级的设备接入，以云服务的形式实现终端设备之间互通互联，进而实现城市物联网终端设备与数据资源的共享，解决智慧城市建设中形成的信息孤岛问题，助力做强“城市大脑”，为智慧城市不同领域提供对应的行业解决方案。'
	},{
		src: '/static/img/steps2.jpg',
		h3: '<em>②</em>电动车防盗监控系统',
		p: '电动车防盗监控系统是基于物联网技术来建设管车系统，系统基于传感层、传输层和应用层三层体系架构。由终端设备、无线网络和中心控制平台构成，利用无线传感网络技术，结合备案登记系统、防盗车牌、有源标签和侦测基站等，让车主、公安人员、车辆间建立关系。'
	},{
		src: '/static/img/steps3.jpg',
		h3: '<em>③</em>物联网管控平台（中心）',
		p: '通过机制与技术手段，解决围绕着公安物联城域网建设方案多业务系统间的应用与分析问题，提供物联网城域域网汇集的海量数据及各项预警、分析结果、协调工作，为指挥决策服务。'
	}];
	export default {
		name: 'shareContent',
		data () {
			return {
				src: '/static/img/download.jpg',
				docs: docs
			}
		}
	}
</script>
<style lang='scss'>
	#download{
		text-align: left;
		position: absolute;
		top: 38%;
		left: 29%;
		z-index: 8;
		color: white;
		font-size: 28px;
		color: #e9e7e5;
		font-weight: 300;
		margin: 0;
		padding: 0;
        animation: none;
	}
	.content {
		.banner {
			position: relative;
			width: 100%;
			top: -13%;
			left: 0;
			margin: 0;
			padding: 0;
			h3+p {
				font-size: 16px;
				color: #e6e5e3;
				font-weight: 300;
				position: absolute;
				top: 44%;
				left: 29%;	
				z-index: 8;
				margin: 0;
				padding: 0;
			}
		}
	}
	.teach{
		margin-bottom: 7%;
		h3 {
			padding: 50px 0;
			font-weight: 500;
			font-size: 30px;
			text-align: center;
			color: #333333;
		}
	}
	.mar{
		margin: 50px 0 50px;
		p {
			line-height: 32px;
			font-size: 14px;
			color: #8d8d8d;
			text-align: center;
		}
	}
	.step{
		display: flex;
		flex-direction: row;
		justify-content: space-around;
	}
	.container {
		width: 300px;
		flex: 0 1 auto;
		img{
			width: 300px;
			height: 300px;
		}
		h3 {
			margin-bottom: 10px;
			text-align: center;
			font-size: 18px;
			color: #333333;
			font-weight: 500;
			padding: 0;
		}
		p {
			line-height: 30px;
			font-size: 14px;
			color: #333333;
			text-align: center;
			opacity: 0.6;
		}
	}
	em{
		font-style: normal;
		font-size: 22px;
		vertical-align: text-bottom;
		line-height: 27px;
	}
</style>