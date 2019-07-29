<template>
  <div class="main">
    <div class="header">
      <h2>{{store.title}}</h2>
      <p class="rate-block">
        <Rate v-model="store.value" :size="12" color="#f44" void-icon="star" void-color="#eee"></Rate>
        <span class="title-text">湘菜</span>
        <span class="title-text">(现摘现做)</span>
      </p>
    </div>
    <div class="header-info">
      <p><b class="iconfont icon-yingyeshijian"></b><span>营业时间: {{store.openTime}}</span></p>
      <p><b class="iconfont icon-didian"></b><span>地址: {{store.address}}</span></p>
      <p><b class="iconfont icon-lianxidianhua"></b><span>联系电话: {{store.contact}}</span></p>
    </div>
    <div class="recommended">
      <div class="recommended-title">推荐菜品/Recommended</div>
    </div>
  </div>
</template>

<script>
  import {
    Button,
    Rate
  } from 'vant'

  export default {
    name: 'Index',
    components: {
      Button,
      Rate
    },
    data() {
      return {
        store: {
          title: "乐活村生态农产餐厅",
          value: 4.5,
          openTime: '11:00~14:00,16:00~18:00',
          address: "湖南省长沙市岳麓区芯城科技园",
          contact: '15516562786/18544732389'
        }
      }
    }
  }
</script>

<style scoped lang="less">
  @import url("../../static/theme.less");
  @import url("//at.alicdn.com/t/font_1320654_yaiy6zhwi6.css");

  .rate-block {
    display: flex;
    justify-content: center;
    align-items: center;

    .title-text {
      font-size: 14px;
      color: #333;
      margin-left: 10px;
    }
  }

  .header-info {
    width: 90%;
    padding: 20px;
    box-sizing: border-box;
    background-color: #f8f8f8;
    border-radius: 8px;
    margin: 0 auto;

    p {
      display: block;
      color: #a1a1a1;
      text-align: left;
      border-bottom: 1px solid #e3e3e3;

      span {
        width: 100px;
      }
    }
  }

  .recommended{
    margin: 20px 0;
    color: @themeColor;
    font-size: @themeFont;
  }
</style>
