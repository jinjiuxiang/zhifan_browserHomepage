<template>
  <div class="m-list-container">
      <div class="m-list-header">
          <div class="m-list-header-btn"></div>
          <img src="../assets/image/logo.svg" alt="">
          <div class="m-list-header-btn">
            <img src="../assets/image/search.svg" alt="">
          </div>
      </div>
      <div class="m-list-info">
        <span>“hd73nxj846gnvmxue7h5nrjf8”</span>,为您查询到3个结果
      </div>
      <div class="m-list-min">
        <mAddress_stencli></mAddress_stencli>
        <mTransaction_stencli></mTransaction_stencli>
        <mBlock_stencli></mBlock_stencli>
      </div>
  </div>
</template>

<script>
    import mAddressStencli from "../../src/components/mdetail/mAddressStencli"
    import mTransactionStencli from "../../src/components/mdetail/mTransactionStencli"
    import mBlockStencli from "../../src/components/mdetail/mBlockStencli"
    export default {
        name: "mSearchList",
        components:{
          mAddress_stencli:mAddressStencli,
          mTransaction_stencli:mTransactionStencli,
          mBlock_stencli:mBlockStencli
        }
    }
</script>

<style scoped>
  .m-list-container{
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .m-list-header{
    display: flex;
    justify-content: space-between;
    width: 100%;
    height: 3.375rem;
    position: fixed;
    background: #ffffff;
    top: 0;
    left: 0;
    border-bottom: 1px solid #C8C8C8;
    align-items: center;
    z-index: 99;
  }
  .m-list-header-btn{
    width: 2.5rem;
    height: 2.5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 8px;
  }
  .m-list-header img{
    width: 9.875rem;
    height: auto;
  }
  .m-list-header-btn img{
    width: 1.5rem;
    height: 1.5rem;
  }
  .m-list-info{
    width: 21.875rem;
    text-align: left;
    margin-top: 5rem;
    font-family: PingFangSC-Regular;
    font-size: 0.875rem;
    color: #151515;
    letter-spacing: 0;
  }
  .m-list-info span{
    color: #00A0E9;
    word-wrap: break-word;

  }
  .m-list-min{
    margin-bottom: 2rem;
  }
  /**/
  @media (min-width: 420px) and (max-width: 740px){
    .m-list-info{
      width: 34.875rem;
    }
  }
  @media (min-width: 750px) and (max-width: 1024px){
    .m-list-info{
      width: 36.875rem;
      margin-top: 6rem;
    }
    .m-list-min{
      margin-bottom: 3rem;
    }
  }
</style>
