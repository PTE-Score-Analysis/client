<template>
	<view>
		<uni-forms
			ref="form"
			:modelValue="formData"
			:rules="rules"
			label-position="top"
		>
			<!-- 头像选择和展示 -->
			<uni-forms-item name="avatar" label-align="center">
				<image
					class="avatar"
					:src="avatarImage"
					v-model="formData.avatar"
				/>
				<button
					type="primary"
					plain="true"
					class="change-avatar"
					@click="chooseImage"
					style="border:none"
				>
					更换头像
				</button>
			</uni-forms-item>
			
			<!-- 用户名输入 -->
			<uni-forms-item name="name">
				<uni-easyinput
					type="text"
					v-model="formData.name"
					placeholder="这里可以更改用户名"
				/>
			</uni-forms-item>
			
			<!-- 提交按钮 -->
			<button
				type="primary"
				@click="submit"
			>
				提交
			</button>
		</uni-forms>
	</view>
</template>
			 
<script>
	export default {
		data() {
			return {
				name: '',
				avatarImage: '/static/my_default.png',
				// 表单数据
				formData: {

				},
				rules: {
					// 对name字段进行必填验证
					name: {
						rules: [{
								required: true,
								errorMessage: '请输入姓名',
							},
							{
								validateFunction:function(rule,value,data,callback){
									// TODO: get后端checkUsername endpoint
									// 如果有重名，则callback('此用户名已被使用')
									// 否则return true
									
									// Demo：检验是否重名
									if (value === 'Max' || value === 'max') {
										callback('此用户名已被使用');
									}
									return true;
								}
							}
						]
					}
				}
			}
		},
		onReady() {
			// 在onReady中设置规则
			this.$refs.form.setRules(this.rules);
		},
		methods: {
			chooseImage() {
				uni.chooseImage({
					count: 1, // 设置为1表示单选
					sizeType: ['compressed'], // 可以指定是原图还是压缩图，默认二者都有
					sourceType: ['album', 'camera'], // 可以指定来源是相册还是相机，默认二者都有
					success: (res) => {
						// tempFilePath可以作为img标签的src属性显示图片
						this.formData.avatar = res.tempFilePaths[0]; // 更新表单数据
						this.avatarImage = res.tempFilePaths[0]; // 更新页面上的头像
					}
				});
			},
			// 触发提交表单
			submit() {
				this.$refs.form.validate().then(res=>{
					console.log('表单成功信息：', res);
					// TODO: post后端save personal endpoint
				}).catch(err =>{
					console.log('表单错误信息：', err);
				})
			}
		}
	}
</script>

<style>
	@import "./personal.scss"; 
</style>