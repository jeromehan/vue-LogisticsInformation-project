<template>
	<div>
		<div class="titleIcon"><span class="iconfont icon-liebiao titleIcon-i"></span><span class="titleIcon-title">定位信息列表</span></div>
		<div class="content">
			<div class="lists" id="wrapper">
				<div class="show" id="scroller">
					<ul class="PositionInfo" id="thelist">
						<li>
							<p class="listTitle"><span class="listDate">2016-10-27</span><span class="listHour">09:20:45</span></p>
							<div>
								<span class="iconfont icon-weizhi positionIcon"></span>
								<p class="positionIconInfo">北京是非得失犯得上犯得上犯得上犯得上犯得上发射点发射点犯得上犯得上犯得上反对法发士大夫士大夫大师傅大师傅大师傅士大夫</p>
								<p class="positionText">备注但是犯得上犯得上犯得上犯得上犯得上发生大师傅大师傅大师傅士大夫但是但是但是但是</p>
							</div>
						</li>
						<li>
							<p class="listTitle"><span class="listDate">2016-10-27</span><span class="listHour">09:20:45</span></p>
							<div>
								<span class="iconfont icon-weizhi positionIcon"></span>
								<p class="positionIconInfo">北京是非得失犯得上犯得上犯得上犯得上犯得上发射点发射点犯得上犯得上犯得上反对法发士大夫士大夫大师傅大师傅大师傅士大夫</p>
							</div>
						</li>
					</ul>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
	export default {
		mounted() {
				this.dropdown();
			},
			methods: {
				dropdown() {
					//上拉加载，下拉刷新
					$(function() {
						var counter = 0;
						// 每页展示4个
						var num = 4;
						var pageStart = 0,
							pageEnd = 0;
						// dropload
						$('.show').dropload({
							scrollArea: window,
							domDown: {
								domClass: 'dropload-down',
								domRefresh: '<div class="dropload-refresh">↑上拉加载更多</div>',
								domLoad: '<div class="dropload-load"><span class="loading"></span>加载中...</div>',
								domNoData: '<div class="dropload-noData">没有更多数据了</div>'
							},
							loadDownFn: function(me) {
								var result = '';
								counter++;
								pageEnd = num * counter;
								pageStart = pageEnd - num;

								for(var i = pageStart; i < pageEnd; i++) {
									result += '<li>' +
										'<p class="listTitle"><span class="listDate">2016-10-27</span><span class="listHour">09:20:45</span></p>' +
										'<div>' +
										'<span class="iconfont icon-weizhi positionIcon"></span>' +
										'<p class="positionIconInfo">北京市石景山区</p>' +
										'<p class="positionText">电风扇第三方第三方第三方第三方</p>' +
										'</div>' +
										'</li>';
									if((i + 1) >= 20) {
										// 锁定
										me.lock();
										// 无数据
										me.noData();
										break;
									}
								}
								// 为了测试，延迟1秒加载
								setTimeout(function() {
									$('.PositionInfo').append(result);
									// 每次数据加载完，必须重置
									me.resetload();
								}, 1000);
							},
							threshold: 50
						});
					});
				}
			}
	}
</script>