<template>
	<view class="container">
	<table>
	      <tr>
	        <td class="zhi">姓名</td>
	        <td class="zhii">:</td>
	        <td class="zhi2">秦少少</td>
	      </tr>
	      <tr>
	        <td class="zhi">年度</td>
	        <td class="zhii">:</td>
	        <td class="zhi2">2023</td>
	      </tr>
	      <tr>
	        <td class="zhi">证书编号</td>
	        <td class="zhii">:</td>
	        <td class="zhi2">GD190023306107</td>
	      </tr>
	      <tr>
	        <td class="zhi">专业系列</td>
	        <td class="zhii">:</td>
	        <td class="zhi2">护理专业</td>
	      </tr>
	      <tr>
	        <td class="zhi">学习情况</td>
	        <td class="zhii">:</td>
	        <td class="zhi2 fudong">
	          <span>已完成专业课<span class="red">97.5</span>学时、</span>
	          <span>已完成专业课<span class="red">97.5</span>学时、</span>
	          <span>已完成专业课<span class="red">97.5</span>学时、</span>
	        </td>
	      </tr>
	      <tr>
	        <td class="zhi">验证结果</td>
	        <td class="zhii">:</td>
	        <td class="zhi2">已完成该年度继续教育任务</td>
	      </tr>
	    </table>
      <button class="mini-btn" type="warn" @click="xianshi" size="mini">证书查看</button>
          <div v-if="xxianshi" style="width: 100%;">
            <image src="../../static/zhengming.jpg" style="width: 100%;" mode="widthFix"></image>
          </div>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				href: 'https://uniapp.dcloud.io/component/README?id=uniui',
        xxianshi:false
			}
		},
		methods: {
      xianshi(){
            if(!this.xxianshi){
              this.xxianshi = !this.xxianshi
            }
            console.log(this.xxianshi)
          }
		}
	}
</script>

<style>
	.container {
		padding:5px 10px ;
    background-color: #ffffff;
	}
  table {
      border-collapse: collapse;
      width: 100%;
      /* font-weight: 700; */
      /* color: #6a6164; */
      color: #333;
      font-size: 16rpx;
    }
    tr{
      line-height: 22rpx;
    }
    td {
      //border: 1px solid #ddd;
    }
    .zhi{
      text-align-last:justify;
      width: 64rpx;
    }
    .red{
      color: red;
    }
    .mini-btn{
      margin-top: 8rpx;
      background-color: #c0ece8;
      color: #437068;
      font-size:16rpx;
    }
    .anniu{
      margin:10px 0;
      color: #437068;
      font-size: 1rem;
      background-color: #c0ece8;
      border-radius: 5px;
      border: 0;
      padding: 5px 10px;
    }
    .fudong{
        display: flex;
        justify-content:space-between;
    }
</style>
