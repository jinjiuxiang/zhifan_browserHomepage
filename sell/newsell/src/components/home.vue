<template>
  <div class="mb-home-container">
    <img class="mb-home-image" src="../assets/image/logoDesc.svg" alt="">
    <div class="mb-home-search">
      <select name="" id="" v-model="selectValue">
        <option value="全币种">全币种</option>
        <option value="BTC">BTC</option>
        <option value="BCH">BCH</option>
        <option value="CTC">CTC</option>
      </select>
      <input type="text" v-model="searchValue" placeholder="区块高度/区块哈希值/交易哈希值/地址哈希值">
      <div class="mb-home-search-btn" @click="getData">
        <img src="../assets/image/search.svg" alt="">
      </div>
    </div>
    <div class="mb-home-footer">
        <div class="mb-home-footer-first">
          <span @touchend="getUS">关于我们</span>
          <span @touchend="getMz">免责声明</span>
        </div>
        <p class="mb-home-footer-second">Copyright © 2017-2018  京ICP备17074962号</p>
    </div>
  </div>
</template>

<script>
    export default {
        name: "home",
        data(){
          return {
            message:"zhe",
            selectValue:"全币种",
            searchValue:""
          }
        },
        methods:{
          getUS(){
            window.location.href = "https://www.chaindigg.com/"
          },
          getMz(){
            window.location.href = "https://www.chaindigg.com/disclaimer"
          },
          getData(){
            const self = this;
            console.log(self.selectValue);
            console.log(self.searchValue);
            if(self.searchValue == ""){
              self.$message.error("查询内容不能为空")
            } else if(self.searchValue != ""){
              self.$router.push({name:"msearchList",params:{searchWord:self.searchValue}})
            }
          }

        }
    }
</script>

<style scoped>
.mb-home-container{
  display: flex;
  width: 100%;
  flex-direction: column;
  align-items: center;
}
  .mb-home-search{
    width: 21.875rem;
    height: 2.5rem;
    background: #FFFFFF;
    border: 0.125rem solid #00A0E9;
    border-radius: 2.5rem;
    margin-top: 1.5rem;
    display: flex;
    justify-content: flex-start;
  }
  .mb-home-search select{
    border: none;
    background: none;
    outline: none;
    ppearance:none;
    -moz-appearance:none;
    -webkit-appearance:none;
    background: url("http://ourjs.github.io/static/2015/arrow.png") no-repeat scroll right center transparent;
    padding-right: 1.25rem;
    font-family: PingFangSC-Regular;
    font-size: 1rem;
    color: #333333;
    line-height: 0.875rem;
    margin-left: 1rem;
  }
  .mb-home-search input{
    border: none;
    outline: none;
    width: 25rem;
    padding-left: 1rem;
    font-size: 1rem;
  }
  .mb-home-search-btn{
    width: 2.5rem;
    height: 2.5rem;
    display: inline-flex;
    justify-content: center;
  }
  .mb-home-footer{
    width: 100%;
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 6.25rem;
    background: #EBEBEB;
    position: absolute;
    left: 0;
    bottom: 0;
    justify-content: center;
  }
  .mb-home-footer-first{
    font-family: PingFangSC-Regular;
    font-size: 1.2rem;
    color: #666666;
    line-height: 1.2rem;
  }
  .mb-home-footer-first span:nth-child(1){
    margin-right: 2.75rem;
  }
  .mb-home-footer-second{
    font-family: PingFangSC-Regular;
    font-size: 1rem;
    color: #999999;
    text-align: center;
    line-height: 1rem;
    margin-top: 1rem;
  }
  /*paid*/
  @media (min-width: 750px) and (max-width: 800px){
    .mb-home-image{
      margin-top: 20rem;
    }
    .mb-home-search{
      width: 34.875rem;
      margin-top: 3rem;
    }
  }
  @media (min-width: 900px) and (max-width: 1024px){
    .mb-home-image{
      margin-top: 14rem;
    }
    .mb-home-search{
      width: 34.875rem;
      margin-top: 3rem;
    }
  }
  /*phone*/
  @media (min-width: 350px) and (max-width: 450px){
    .mb-home-image{
      width: 12.875rem;
      height: auto;
      margin-top: 12rem;
    }
    .mb-home-search{
      width: 22rem;
      height: 2.5rem;
    }
    .mb-home-search select{
      font-size: 0.75rem;
      padding-right: 1rem;
    }
    .mb-home-search input{
      font-size: 0.75rem;
      padding-left: 0.25rem;
      width: 20rem;
    }
    .mb-home-search-btn{
      align-items: center;
    }
    .mb-home-search-btn img{
      width: 1rem;
      height: 1rem;
    }
    .mb-home-footer{
      height: 4.25rem;
    }
    .mb-home-footer-first{
      font-size: 0.75rem;
    }
    .mb-home-footer-second{
      font-size: 0.75rem;
    }
  }
  @media (min-width: 460px) and (max-width: 749px){

    .mb-home-footer{
      height: 4.25rem;
    }
    .mb-home-footer-first{
      font-size: 0.75rem;
    }
    .mb-home-footer-second{
      font-size: 0.75rem;
    }
    .mb-home-image{
      margin-top: 4rem;
    }
    .mb-home-search{
      width: 32rem;
      height: 2.5rem;
      margin-top: 3rem;
    }
    .mb-home-search select{
      font-size: 0.75rem;
      padding-right: 1.5rem;
    }
    .mb-home-search input{
      font-size: 0.75rem;
      padding-left: 1rem;
      width: 24rem;
    }
    .mb-home-search-btn{
      align-items: center;
    }
    .mb-home-search-btn img{
      width: 1rem;
      height: 1rem;
    }
    .mb-home-image{
      width: 17rem;
    }
  }
  @media (min-width: 801px) and (max-width: 820px){

  .mb-home-footer{
    height: 4.25rem;
  }
  .mb-home-footer-first{
    font-size: 0.75rem;
  }
  .mb-home-footer-second{
    font-size: 0.75rem;
  }
  .mb-home-image{
    margin-top: 4rem;
  }
  .mb-home-search{
    width: 32rem;
    height: 2.5rem;
    margin-top: 3rem;
  }
  .mb-home-search select{
    font-size: 0.75rem;
    padding-right: 1.5rem;
  }
  .mb-home-search input{
    font-size: 0.75rem;
    padding-left: 1rem;
    width: 24rem;
  }
  .mb-home-search-btn{
    align-items: center;
  }
  .mb-home-search-btn img{
    width: 1rem;
    height: 1rem;
  }
  .mb-home-image{
    width: 17rem;
  }
}

</style>
