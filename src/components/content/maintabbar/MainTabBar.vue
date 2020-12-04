<template>
	<tab-bar>
		<tab-bar-item path="/home" color="#ff8198">
			<img slot="tab-img" src="~assets/img/tabbar/home.svg" alt="" />
			<img slot="tab-img-active" src="~assets/img/tabbar/home_active.svg" alt="" />
			<div slot="tab-item">首页</div>
		</tab-bar-item>
		<tab-bar-item path="/category" color="#ff8198">
			<img slot="tab-img" src="~assets/img/tabbar/category.svg" alt="" />
			<img slot="tab-img-active" src="~assets/img/tabbar/category_active.svg" alt="" />
			<div slot="tab-item">分类</div>
		</tab-bar-item>
		<tab-bar-item path="/shopcart" color="#ff8198">
			<img slot="tab-img" src="~assets/img/tabbar/shopcart.svg" alt="" />
			<img slot="tab-img-active" src="~assets/img/tabbar/shopcart_active.svg" alt="" />
			<div slot="tab-item">购物车</div>
		</tab-bar-item>
		<tab-bar-item path="/profile" color="#ff8198">
			<img slot="tab-img" src="~assets/img/tabbar/profile.svg" alt="" />
			<img slot="tab-img-active" src="~assets/img/tabbar/profile_active.svg" alt="" />
			<div slot="tab-item">我的</div>
		</tab-bar-item>
	</tab-bar>
</template>

<script>
import TabBar from '@/components/common/tabbar/TabBar'
import TabBarItem from '@/components/common/tabbar/TabBarItem'
export default {
	name: 'MainTabBar',
	data() {
		return {}
	},
	components: {
		TabBar,
		TabBarItem,
	},
}
</script>

<style></style>
