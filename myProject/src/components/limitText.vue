<template>
	<div class="extraText">
		<p><textarea v-on:keyup="checkWord" name="content" placeholder="填写备注仅限于您记录当前定位信息..." rows="4"></textarea></p>
		<div class="extraTextScore">(<span id="wordCheck">0</span>/100)</div>
		<div class="submitButtom" v-on:click="subForm()">提交</div>
	</div>
</template>
<script>
	export default {
		data() {
				return {

				}
			},
			methods: {
				checkWord: function(c) {
					var len = 100;
					var str = c.target.value;
					var myLen = 0;
					var i = 0;
					for(;
						(i < str.length) && (myLen <= 100 * 2); i++) {
						if(str.charCodeAt(i) > 0 && str.charCodeAt(i) < 128)
							myLen++;
						else
							myLen += 2;
					}
					var wck = document.getElementById('wordCheck');
					if(myLen > len * 2) {
						c.target.value = str.substring(0,i- 1);
					} else {
						wck.innerHTML = 100 - (Math.floor((len * 2 - myLen) / 2));
					}
				}
			}
	}
</script>