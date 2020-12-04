<template>
	<div id="home">
		<nav-bar class="nav-bar">
			<div slot="center">购物街</div>
		</nav-bar>
		<home-swiper :banner="banner"></home-swiper>
		<recommend-view :recommend="recommend"></recommend-view>
	</div>
</template>

<script>
import NavBar from '@/components/common/navbar/NavBar'
import { getHomeMultidata } from 'network/home'
import HomeSwiper from '@/views/home/childComps/HomeSwiper'
import RecommendView from '@/views/home/childComps/RecommendView'
export default {
	data() {
		return {
			banner: [],
			recommend: [],
		}
	},
	components: {
		NavBar,
		HomeSwiper,
		RecommendView,
	},
	async created() {
		const { data: res } = await getHomeMultidata()
		this.banner = res.banner.list
		this.recommend = res.recommend.list
	},
}
</script>

<style scoped>
.nav-bar {
	background-color: var(--color-tint);
	color: #fff;
}
</style>
