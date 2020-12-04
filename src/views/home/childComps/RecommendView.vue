<template>
	<div id="recommend">
		<div v-for="item in recommend" :key="item.acm" class="recommend-item">
			<a :href="item.link">
				<img :src="item.image" alt="" />
			</a>
			<div>{{ item.title }}</div>
		</div>
	</div>
</template>

<script>
export default {
	props: {
		recommend: {
			type: Array,
			default() {
				return []
			},
		},
	},
}
</script>

<style>
#recommend {
	display: flex;
	width: 100%;
	font-size: 12px;
	text-align: center;
	padding: 10px 0 20px 0;
	border-bottom: 10px solid #eee;
}
.recommend-item {
	flex: 1;
}
.recommend-item img {
	width: 70px;
	height: 70px;
	margin-bottom: 10px;
}
</style>
