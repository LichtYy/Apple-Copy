<template>
  <div :class="imgDivClassName">
    <div class="section-content2-text">
      <h2 class="sc2-text1">iPhone 14 Pro</h2>
      <h3 class="sc2-text2">强力出圈</h3>
      <div class="sc2-text3">
        <a href="https://www.apple.com.cn/iphone-14-pro/"
          >进一步了解<i class="el-icon-arrow-right"></i
        ></a>
        <a href="https://www.apple.com.cn/cn/shop/goto/buy_iphone/iphone_14_pro"
          >购买<i class="el-icon-arrow-right"></i
        ></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionContent2",
  data() {
    return {
      baseClassName: "section-content2",
      imgClassName: "imgLarge",
    };
  },
  computed: {
    imgDivClassName() {
      return this.baseClassName + " " + this.imgClassName;
    },
  },
  methods: {
    setClassName() {
      const visibleSrceenWidth = document.body.clientWidth;
      if (visibleSrceenWidth >= 1096) this.imgClassName = "imgLarge";
      else if (visibleSrceenWidth >= 735) this.imgClassName = "imgMedium0";
      else if (visibleSrceenWidth >= 430) this.imgClassName = "imgMedium1";
      else this.imgClassName = "imgMedium2";
    },
  },
  mounted() {
    this.setClassName();
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.section-content2 {
  width: 100%;
  height: 100%;
  background-repeat: no-repeat;
  background-position: center bottom;
  background-size: cover;
  padding-top: 61px;
}
.section-content2-text {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
  text-align: center;
  vertical-align: middle;
  align-items: center;
}
.sc2-text1 {
  color: rgb(245, 245, 247);
  font-size: 48px;
  font-weight: 600;
  line-height: 52px;
}
.sc2-text2 {
  color: rgb(245, 245, 247);
  font-size: 24px;
  font-weight: 400;
  line-height: 28px;
  margin-top: 5px;
}
.sc2-text3 {
  font-size: 16px;
  font-weight: 400;
  line-height: 23px;
  margin-top: 14px;
}
.sc2-text3 a {
  text-decoration: none;
  color: rgb(41, 151, 255);
  padding-right: 20px;
}
.sc2-text3 a:hover {
  text-decoration: underline;
}
.imgLarge {
  min-width: 1069px;
  min-height: 650px;
  max-height: 750px;
  background-image: url(https://www.apple.com.cn/home/heroes/iphone-14-pro/images/hero_iphone14pro_spring__9xo85pm6sbmm_largetall_2x.jpg);
}
.imgMedium0 {
  max-width: 1068px;
  height: 650px;
  background-image: url(https://www.apple.com.cn/home/heroes/iphone-14-pro/images/hero_iphone14pro_spring__9xo85pm6sbmm_mediumtall_2x.jpg);
}
.imgMedium1 {
  max-width: 734px;
  height: 500px;
  background-image: url(https://www.apple.com.cn/home/heroes/iphone-14-pro/images/hero_iphone14pro_spring__9xo85pm6sbmm_mediumtall_2x.jpg);
}
.imgMedium2 {
  max-width: 430px;
  height: 500px;
  background-image: url(https://www.apple.com.cn/home/heroes/iphone-14-pro/images/hero_iphone14pro_spring__9xo85pm6sbmm_mediumtall_2x.jpg);
}
</style>
