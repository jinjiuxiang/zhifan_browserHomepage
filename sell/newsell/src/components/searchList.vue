<template>
    <div class="pc-list-container">
        <div class="pc-list-header">
            <div class="pc-list-header-left">
              <img src="../assets/image/logo.svg" @click="getHome" alt="">
              <div class="pc-list-header-search">
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
            <div class="pc-list-header-right">
                <span>登录</span>
                <span>注册</span>
            </div>
        </div>
        <div class="pc-list-main">
            <div class="pc-list-result">
              <span>“</span><span>{{params.searchWord}}</span><span>”</span>,为您查询到3个结果
            </div>
            <div class="pc-list-stencli">
               <address_stencli></address_stencli>
               <transaction_stencli></transaction_stencli>
               <block_stencli></block_stencli>
            </div>
        </div>
    </div>
</template>

<script>
    import addressStencli from "../../src/components/detail/addressStencli"
    import transactionStencli from "../../src/components/detail/transactionStencli"
    import blockStencli from "../../src/components/detail/blockStencli"
    export default {
        name: "searchList",
        components:{
          address_stencli:addressStencli,
          transaction_stencli:transactionStencli,
          block_stencli:blockStencli
        },
        data(){
          return {
            parentMessage:"parent",
            selectData:"全币种",
            params:this.$route.params,
            searchValue:""
          }
        },
        methods:{
            getSearch(){
              const self = this;
              console.log(self.searchValue);
              console.log(self.selectData);
              if(self.searchValue == ""){
                self.$message.error("搜索内容不能为空")
              } else if(self.selectData != "全币种"){
                window.location.href = "http://www.baidu.com"
              }else {
                // self.$router.push({name:"searchList",params:{searchWord:self.searchValue}})
                self.params.searchWord = self.searchValue;
              }
            },
            getHome(){
              const self = this;
              self.$router.push({name:"home"})
            }
        },
        mounted(){
          console.log(this.params);
        }
    }
</script>

<style scoped>
  .pc-list-header{
    width: 100%;
    height: 64px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px #F1F1F2 solid;
  }
  .pc-list-header img{
    cursor: pointer;
  }
  .pc-list-header-left{
    display: flex;
    margin-left: 3rem;
  }
  .pc-list-header-search{
    width: 30rem;
    height: 2rem;
    background: #FFFFFF;
    border: 0.125rem solid #00A0E9;
    border-radius: 2.5rem;
    margin-left: 3.75rem;
    display: flex;
    align-items: center;
    justify-content: flex-start;
  }
  .pc-list-header-search select{
    border: none;
    background: none;
    outline: none;
    ppearance:none;
    -moz-appearance:none;
    -webkit-appearance:none;
    background: url("http://ourjs.github.io/static/2015/arrow.png") no-repeat scroll right center transparent;
    padding-right: 1.25rem;
    font-family: PingFangSC-Regular;
    font-size: 0.875rem;
    color: #333333;
    line-height: 0.875rem;
    margin-left: 1rem;
  }
  .pc-list-header-search input{
    width: 22rem;
    padding-left: 1rem;
    height: 2rem;
    outline: none;
    border: none;
    font-size: 0.875rem;
  }
  .pc-list-header-search img{
   width: 1.125rem;
  }
  .pc-list-header-right span{
    opacity: 0.8;
    font-family: PingFangSC-Regular;
    font-size: 1rem;
    color: #333333;
    line-height: 1rem;
    margin-right: 1.5rem;
  }
  /**/
  .pc-list-result{
    display: flex;
    justify-content: flex-start;
    padding: 0 5%;
    margin: 3rem 0 1rem 0;
  }
  .pc-list-result span{
    ont-family: PingFangSC-Regular;
    font-size: 1rem;
    color: #00A0E9;
    letter-spacing: 0;
  }
  /**/
  .pc-list-stencli{
    width: 100%;
    box-sizing: border-box;
    padding:  0 5%;
  }
</style>
