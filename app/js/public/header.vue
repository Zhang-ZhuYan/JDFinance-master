<template>
    <div class="header">
        <div class="left">
            <em>登录</em>&nbsp;|&nbsp;<em>注册</em>
        </div>
        <btn :cname="'right'">下载APP</btn>
    </div>
</template>
<script>
import btn from '../core/btn'
export default {
    components: {
        btn
    }
}
</script>
<style lang="scss" scoped>
.header{
    height: 120px;
    position: fixed;
    left: 0;
    top: 0;
    right: 0;
    background: url('https://storage.360buyimg.com/base/images/jdjr-logo/logo-jr-r.png?20181203') 50% no-repeat;
    background-size: 30% auto;
    z-index: 100;
    background-color: #ffffff;
    .left{
        font-size: 28px;
        height: 30px;
        margin: 45px 18px;
        float: left;        
        >em{
            font-style: normal;
        }
    }
    .right{
        float: right;
        font-size: 28px;
        line-height: 48px;
        margin: 26px 18px;
    }
}
</style>