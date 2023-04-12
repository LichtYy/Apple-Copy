<template>
  <div id="app">
    <AdvWrapper />
    <NavBar ref="navBar" />
    <SectionContent1 />
    <SectionContent2 ref="sectionContent2" />
  </div>
</template>

<script>
import AdvWrapper from "./components/AdvWrapper.vue";
import NavBar from "./components/nav/NavBar.vue";
import SectionContent1 from "./components/SectionContent1.vue";
import SectionContent2 from "./components/SectionContent2.vue";
export default {
  name: "App",
  components: {
    AdvWrapper,
    NavBar,
    SectionContent1,
    SectionContent2,
  },
  mounted() {
    window.onresize = () => {
      this.$refs.sectionContent2.setClassName();
      this.$refs.navBar.setShowNavItem();
    };
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
}
html,
body {
  height: 100%;
  width: 100%;
  font-family: "SF Pro SC", "SF Pro Text", "SF Pro Icons", "PingFang SC",
    "Helvetica Neue", "Helvetica", "Arial", sans-serif;
}
#app {
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
}
</style>
