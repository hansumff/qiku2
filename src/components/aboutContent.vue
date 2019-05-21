<template>
	<div class='content'>
		<div class='banner'>
			<h3 id='about'>愿景 物联世界<br>使命 智慧玩家</h3>
			<img :src='src' />
		</div>
		<div>
			<div class='mar' v-for='item in docs'>
				<h3>{{item.h3}}</h3>
				<p class='word'>{{item.p1}}</p>
				<p class='word'>{{item.p2}}</p>
				<p class='word'>{{item.p3}}</p>
				<p class='word'>{{item.p4}}</p>
			</div>
			
		</div>
	</div>
</template>
<script>
	const docs = [{
		h3: '公司简介',
		p1: '陕西骑酷物联网科技股份有限公司属上海骑酷科技总部的分支机构，是一家专业从事RFID研发与智能城市系统建设，集自主研发、设计、制造、维护于一体的专业科技型、创新型公司。',
		p2: '公司拥有多项领先技术，集设备自主研发与指导，软件应用设计，系统建设与运营为一体的，将物联网应用与云计算服务',
		p3: '完美结合，开创了 "云+端" 的技术服务模式，是新一代领先信息技术应用企业。',
		p4: '公司致力于智慧城市建设的研发、创新，自主研发的物联网治安监管平台也已经以 “资源共享，合作共赢” 的原则与全国各地公安部门广泛展开合作。'
	},{
		h3: '企业文化',
		p1: '未来10年，物联网将持续带动数字企业创新的商机，国际研究暨顾问机构Gartner最新公布2018年至2023年引领数字企业创新的十大',
		p2: '让外来人融不进来，也让原住民忘了城市本来的样子，',
		p3: '正因如此，ofo 共享单车怀揣“随时随地有车骑”的朴素愿景来到城市，试图满足人们短途代步的需求，',
		p4: '更用这辆单车，重新丈量人们经过的每一条路线，找寻与城市的全新连接方式。'
	},{
		h3: '资质荣誉',
		p1: 'ofo 以开放平台和共享精神，欢迎用户共享自己的单车加入 ofo，以互联网创新模式调动城市单车存量市场，',
		p2: '提高自行车使用效率，为城市节约更多空间；',
		p3: '在未来， ofo 希望不生产自行车，只连接自行车，让人们在全世界的每一个角落都可以通过 ofo 解锁自行车，',
		p4: '随时随地有车骑，满足短途代步的需求。'
	}];
	export default {
		name: 'shareContent',
		data () {
			return {
				src: '/static/img/about.jpg',
				docs: docs
			}
		}
	}
</script>
<style lang='scss'>
	#about{
		text-align: left;
		position: absolute;
		top: 16%;
		left: 20%;
		z-index: 8;
		color: white;
		font-size: 34px;
        line-height: 130%;
        animation: fadeIn 2s 0.5s ease both;
	}
	.mar{
		margin: 50px 0 50px;
		h3 {
			font-size: 36px;
			padding: 42px 0 26px;
			font-weight: 500;
			color: #b62922;
		}
		p {
			line-height: 32px;
			font-size: 14px;
			color: #8d8d8d;
			text-align: center;
		}
	}
</style>