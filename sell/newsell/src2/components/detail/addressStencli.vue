<template>
  <div class="pc-stencli-container">
      <div class="pc-stencli-header">
        <div class="pc-stencli-header-left">
          <img src="../../assets/image/bch.svg" alt="">
          <span class="pc-stencli-name">BCH</span>
        </div>
        <div class="pc-stencli-header-right">
          <span class="pc-stencli-label">地址：</span>
          <span class="pc-stencli-text">17A16QmavnUfCW11DAApiJxp7ARnxN5pGX</span>
        </div>
      </div>
      <div class="pc-stencli-main">
        <div class="pc-stencli-main-left">
          <div class="pc-stencli-main-box">
            <span class="pc-stencli-label">总收入：</span>
            <span class="pc-stencli-text">100&nbsp;BTC</span>
          </div>
          <div class="pc-stencli-main-box">
            <span class="pc-stencli-label">余额：</span>
            <span class="pc-stencli-text">15&nbsp;BTC</span>
          </div>
        </div>
        <div class="pc-stencli-main-right">
          <div class="pc-stencli-main-box">
            <span class="pc-stencli-label">总交易次数：</span>
            <span class="pc-stencli-text">10次</span>
          </div>
          <div class="pc-stencli-main-box">
            <span class="pc-stencli-label">最新交易：</span>
            <span class="pc-stencli-text">+200 BTC/2018.08.24  15:55:32</span>
          </div>
        </div>
      </div>
      <span class="pc-stencli-detail">查看详情</span>
  </div>
</template>

<script>
    export default {
        name: "addressStencli",
        props:{
          message:Object
        }
    }
</script>

<style scoped>
  .pc-stencli-container{
    width: 100%;
    height: 9.5rem;
    margin-top: 1.57rem;
    background: #FFFFFF;
    border: 1px solid rgba(0,160,233,0.2);
    border-radius: 0.5rem;
    position: relative;
  }
  .pc-stencli-header{
    width: 100%;
    height: 3rem;
    background-color: rgba(0,160,233,0.2);
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-radius: 0.5rem 0.5rem 0 0;
  }
  .pc-stencli-header-left{
    display: flex;
    align-items: center;
    box-sizing: border-box;
    padding-left: 2.5rem;
    width: 36%;
  }
  .pc-stencli-header-right{
    flex: 1;
    display: flex;
    justify-content: flex-start;
  }
  .pc-stencli-name{
    font-family: PingFangSC-Regular;
    font-size: 1rem;
    color: #333333;
    margin-left: 0.5rem;
  }
  .pc-stencli-label{
    font-family: PingFangSC-Regular;
    font-size: 1rem;
    color: #999999;
    line-height: 1rem;
  }
  .pc-stencli-text{
    font-family: PingFangSC-Regular;
    font-size: 1rem;
    color: #151515;
    line-height: 1rem;
  }
  /**/
  .pc-stencli-main{
    display: flex;
  }
  .pc-stencli-main-left{
    width: 36%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding-left: 2.5rem;
    box-sizing: border-box;
  }
  .pc-stencli-main-right{
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
  .pc-stencli-main-box{
    margin-top: 1.5rem;
  }
  .pc-stencli-main-box:nth-child(2){
    margin-top: 1.1rem;
  }
  .pc-stencli-detail{
    font-family: PingFangSC-Regular;
    font-size: 1rem;
    color: #00A0E9;
    line-height: 1rem;
    position: absolute;
    right: 2.5rem;
    bottom: 2.75rem;
    cursor: pointer;
  }
  @media (max-width: 1280px) {
    .pc-stencli-main-left{
      width: 30%;
    }
    .pc-stencli-header-left{
      width: 30%;
    }
  }
</style>
