<template>
  <div>
     <view class="userinfo">
    <view class="userinfo-avatar">
    <open-data type="userAvatarUrl"></open-data>
    </view>
    <open-data type="userNickName"></open-data>
    </view>
  <i-panel title="请登录账号">
      <i-input :value="numble" @change="changeNumble($event)" title="账号" autofocus placeholder="请输入账号" maxlength="50" />
      <i-input :value="name" @change="changeName($event)" title="名称" placeholder="请输入名称" maxlength="30" />
      <i-input :value="password" @change="changePassword($event)" title="密码" placeholder="请输入密码" maxlength="50" />
    </i-panel>
    <i-button @click="handleClick" type="warning" size="default">登录</i-button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      numble:"",
      name:"",
      password:""
    }
  },
  methods: {
    changeName (event) {
      this.name = event.mp.detail.detail.value
    },
    changeNumble (event) {
      this.numble = event.mp.detail.detail.value
    },
    changePassword (event) {
      this.password = event.mp.detail.detail.value
    },
    handleClick () {
      if (this.name && this.reason && this.address) {
        wx.showToast({
          title: '登陆成功' + this.name,
          icon: 'success',
          duration: 2000
        })
        // TODO:将账号信息数据提交到云数据库
      } else {
        wx.showToast({
          title: '信息不完整',
          icon: 'none',
          duration: 2000
        })
      }
    }
  },
  created () {
  }
}
</script>

<style scoped>
.userinfo {
  position: relative;
  width: 750rpx;
  height: 320rpx;
  color: #666;
  display: flex;
  flex-direction: column;
  align-items: center;
}
 
.userinfo-avatar {
  overflow:hidden;
  display: block;
  width: 160rpx;
  height: 160rpx;
  margin: 20rpx;
  margin-top: 50rpx;
  border-radius: 50%;
  border: 2px solid #fff;
  box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.2);
}
.tips {
  padding: 20pt;
  font-size: 10pt;
  color:darkorange;
}
</style>