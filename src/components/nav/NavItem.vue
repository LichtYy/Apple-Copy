<template>
  <div class="nav-item" @mouseleave="itemLeave">
    <div class="nav-item-text" @mouseenter="itemEnter">
      {{ itemText }}
    </div>
    <el-collapse-transition>
      <ul class="nav-item-menu transition-box" v-show="menuVisible">
        <li v-for="group in menu" :key="group.groupName">
          <div class="nav-item-menu-group-name">{{ group.groupName }}</div>
          <div
            class="nav-item-menu-group-selection"
            v-for="selection in group.groupSelections"
            :key="selection"
          >
            {{ selection }}
          </div>
        </li>
      </ul>
    </el-collapse-transition>
  </div>
</template>

<script>
export default {
  name: "NavItem",
  props: ["itemText", "menu"],
  data() {
    return {
      value: "",
      menuVisible: false,
    };
  },
  methods: {
    itemEnter() {
      this.menuVisible = true;
    },
    itemLeave() {
      this.menuVisible = false;
    },
    mounted() {
      this.itemLeave();
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.nav-item-text {
  height: 100%;
  display: flex;
  align-items: center;
}
.nav-item-text:hover {
  color: #ffffff;
}
ul.nav-item-menu {
  position: absolute;
  left: 0;
  width: 100%;
  display: flex;
  z-index: 1;
  background-color: #161617;
  line-height: 25px;
  padding-top: 40px;
}
li:first-child {
  font-size: 24px;
  font-weight: 600;
  line-height: 40px;
  padding-left: 220px;
}
li {
  list-style: none;
  padding-bottom: 60px;
  padding-right: 10%;
}
.nav-item-menu-group-name {
  color: #86868b;
  font-size: 12px;
  line-height: 16px;
  padding-bottom: 10px;
}
.nav-item-menu-group-selection {
  color: #e8e8ed;
}
</style>
