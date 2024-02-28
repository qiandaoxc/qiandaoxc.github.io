<template>
	<view class="body">
		<view class="top">
			<view class="search-container">
				</view> -->
				<input class="search-input" type="text" placeholder="Search..."/>
				<view class="search-button">
					<image src="/static/icon/icon.svg" />
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				time:new Date().toLocaleString()
			}
		},
		created() {
		setInterval(() => {
		    this.time = new Date().toLocaleString();
		  }, 1000);
		}
	}
</script>


<style>
page{
	--margin-left-color:#70e1f5;
	--margin-right-color:#ffd194;
	--container-background-color:#406370;
	--rocket-unfold-color:#fcb251;
}
.body{
	height: 100%;
	width: 100%;
	background-image: linear-gradient(90deg, var(--margin-left-color) 0%,var(--margin-right-color) 100%);
	position: fixed;
}
.top{
	height: 150rpx;
	top: 50%;
	left: 50%;
	position: absolute;
	transform: translate(-50%, -50%);
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
}
.search-container {
	height: 120rpx;
	border-radius: 60rpx;
	background-color: var(--container-background-color);
	display: flex;
	flex-direction: row;
	justify-content: space-between;
  align-items: center;
}
.search-icon{
	width: 0rpx;
	height: 75rpx;
	display: flex;
	flex-direction: row;
	justify-content: center;
	align-items: center;
}
.search-icon image{
	width: 75rpx;
	height: 75rpx;
}
.search-input {
	border: none;
	background: none;
	color: white;
	outline: none;
	transition: 0.4s;
	height: 75rpx;
	width: 0rpx;
  border-radius: 10rpx;
}

.search-button {
	width: 120rpx;
	height: 120rpx;
	display: flex;
	flex-direction: row;
	justify-content: center;
	align-items: center;
	border-radius: 60rpx;
}
.search-button image {
	width: 70rpx;
	height: 70rpx;
	padding:15rpx;
	border-radius:50%;
}
.search-input-focused{
	width: 400rpx;
	padding-left: 30rpx;
}
/* hover 操作的直接子元素 */
/* 当鼠标悬停在 .search-contain时，改变。search-input的样式 */
.search-container:hover > .search-input {
	width: 400rpx;
	padding-left: 30rpx;
}
.search-container:hover > .search-icon {
	width: 75rpx;
	padding-left: 30rpx;
}
</style>
