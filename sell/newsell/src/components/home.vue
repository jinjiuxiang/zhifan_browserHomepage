<template>
  <div class="home-container">
    <div class="pc-home-container">
      <div class="pc-home-header">
        <span>登录</span>
        <span>注册</span>
      </div>
      <div class="pc-home-main">
        <div>
          <div class="pc-home-image">
            <img src="../assets/image/logoDesc.svg" alt="">
          </div>
          <div class="pc-home-search">
            <select name="" id="" v-model="selectData">
              <option value="全币种">全币种</option>
              <option value="BTC">BTC</option>
              <option value="BCH">BCH</option>
              <option value="CTC">CTC</option>
            </select>
            <input type="text" v-model="searchValue" placeholder="区块高度/区块哈希值/交易哈希值/地址哈希值">
            <img src="../assets/image/search.svg" @click="getSearch" alt="">
          </div>
        </div>
        <img class="bottom-image" src="../assets/image/bottom.svg" alt="">
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
            selectData:"全币种",
            searchValue:"",
          }
        },
        methods:{
          getSearch(){
            const self  = this;
            console.log(self.selectData);
            console.log(self.searchValue);
            if(self.searchValue == ""){
              self.$message.error("搜索内容不能为空")
            } else if(self.selectData != "全币种"){
              window.location.href = "http://www.baidu.com"
            }else {
              self.$router.push({name:"searchList",params:{searchWord:self.searchValue}})
            }
          }
        }
    }
</script>

<style scoped>
  .pc-home-header{
    height: 3.75em;
    width: 100%;
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }
  .pc-home-header span{
    opacity: 0.8;
    font-family: PingFangSC-Regular;
    font-size: 1rem;
    color: #333333;
    line-height: 1rem;
    margin-right: 2.5rem;
  }
  .pc-home-main{
    display: flex;
    flex-direction:column;
    align-items: center;
    overflow: auto;
    justify-content: space-between;
  }
  .pc-home-search{
    width: 37.5rem;
    height: 3.25rem;
    background: pink;
    display: flex;
    align-items: center;
    background: #FFFFFF;
    border: 0.125rem solid #00A0E9;
    border-radius: 2.5rem;
    margin-top: 3rem;
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
    padding-right: 1.25rem;
    ont-family: PingFangSC-Regular;
    font-size: 1rem;
    color: #333333;
    line-height: 1rem;
    margin-left: 1.5rem;
  }
  .pc-home-search input{
    width: 25rem;
    padding-left: 1rem;
    height: 2rem;
    outline: none;
    border: none;
    font-size: 1rem;
  }
  .pc-home-search img{
    margin-left: 3.5rem;
  }
  .pc-home-image{
    margin-top: 12.5rem;
  }
  .pc-home-desc{
    font-family: PingFangSC-Regular;
    font-size: 1rem;
    color: #666666;
    line-height: 1rem;
    margin-top: 1.5rem;
    display: flex;
    justify-content: center;
  }
  /**/
  .bottom-image{
    width: 100%;
    height: auto;
  }
  @media (max-height:770px) and (max-width: 1100px){
    .bottom-image{
      display: flex;
      margin-top: 6.25rem;
      width: 1100px;
      /*position: absolute;*/
      /*left: 0;*/
      /*bottom: 0;*/
    }
  }
  @media (max-height:770px) and (min-width: 1100px){
    .bottom-image{
      display: flex;
      margin-top: 6.25rem;
      width: 100%;
      /*position: absolute;*/
      /*left: 0;*/
      /*bottom: 0;*/
    }
  }
  @media (min-height:770px) and (min-width: 1100px){
    .bottom-image{
      /*margin-top: 6.25rem;*/
      /*width: 1100px;*/
      position: absolute;
      left: 0;
      bottom: 0;
    }
  }
</style>
