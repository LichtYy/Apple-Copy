<template>
  <div class="adv-wrapper">
    <span class="adv-wrapper-text">&lt;广告&gt;</span>
  </div>
</template>

<script>
export default {
  name: "AdvWrapper",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.adv-wrapper {
  background-color: #282829;
  height: 48px;
  width: 100%;
  color: #eeeeee;
}
.adv-wrapper-text {
  display: flex;
  height: 100%;
  align-items: center;
  float: right;
  margin-right: 220px;
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  font-size: 12px;
}
</style>
