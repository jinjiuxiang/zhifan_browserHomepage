<template>
  <div class="home-container">
    <div class="pc-home-container">
      <div class="pc-home-header">
        <span>登录</span>
        <span>注册</span>
      </div>
      <div class="pc-home-main">
          <div class="pc-home-search">
            <select name="" id="">
              <option value="">BTC</option>
              <option value="">BCH</option>
              <option value="">CTC</option>
            </select>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "home",
        data(){
          return {
            message:"zhe",
            options: [{
              value: '选项1',
              label: '黄金糕'
            }, {
              value: '选项2',
              label: '双皮奶'
            }, {
              value: '选项3',
              label: '蚵仔煎'
            }, {
              value: '选项4',
              label: '龙须面'
            }, {
              value: '选项5',
              label: '北京烤鸭'
            }],
            value: ''
          }
        },
        methods:{

        }
    }
</script>

<style scoped>
  .pc-home-container{
    height: 60px;
    width: 100%;
    background: skyblue;
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }
  .pc-home-main{
    position: absolute;
    top: 60px;
    left: 0;
    right: 0;
    bottom: 0;
    background: red;
    display: flex;
  }
  .pc-home-search{
    width: 100%;
    height: 52px;
    background: red;
    display: flex;
    align-items: center;
  }
  select::-ms-expand { display: none; }
  .pc-home-search select{
    border: none;
    background: none;
    outline: none;
    ppearance:none;
    -moz-appearance:none;
    -webkit-appearance:none;
    background: url("http://ourjs.github.io/static/2015/arrow.png") no-repeat scroll right center transparent;
    padding-right: 14px;
    ont-family: PingFangSC-Regular;
    font-size: 16px;
    color: #333333;
    line-height: 16px;
  }
</style>
