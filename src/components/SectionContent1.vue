<template>
  <div class="section-content1">
    <span class="section-content1-text"
      >用 iPhone 11 或后续机型来换购 iPhone 14 或 iPhone 14 Pro，预计可享 RMB
      1200 至 RMB 5250 的折抵优惠<sup><a href="#footnote-1">1</a></sup
      >。
      <a href="https://www.apple.com.cn/cn/shop/goto/buy_iphone"
        >换购 iPhone<i class="el-icon-arrow-right"></i></a
    ></span>
  </div>
</template>

<script>
export default {
  name: "SectionContent1",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.section-content1 {
  background-color: #f5f5f7;
  height: 48px;
  width: 100%;
  text-align: center;
  display: flex;
  align-items: center;
  color: #1d1d1f;
}
.section-content1-text {
  height: 50%;
  font-size: 14px;
  width: 100%;
}
.section-content1-text a {
  text-decoration: none;
  color: rgb(41, 151, 255);
  padding-right: 5px;
}
.section-content1-text sup {
  font-size: 5px;
}
.section-content1-text a:hover {
  text-decoration: underline;
}
</style>
