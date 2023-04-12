<template>
  <div id="nav-bar" :class="navBarClassName">
    <ul class="nav-item-list">
      <li class="nav-bar-icon apple-icon">
        <a href="https://www.apple.com.cn/">
          <svg
            height="44"
            viewBox="0 0 14 44"
            width="14"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="m13.0729 17.6825a3.61 3.61 0 0 0 -1.7248 3.0365 3.5132 3.5132 0 0 0 2.1379 3.2223 8.394 8.394 0 0 1 -1.0948 2.2618c-.6816.9812-1.3943 1.9623-2.4787 1.9623s-1.3633-.63-2.613-.63c-1.2187 0-1.6525.6507-2.644.6507s-1.6834-.9089-2.4787-2.0243a9.7842 9.7842 0 0 1 -1.6628-5.2776c0-3.0984 2.014-4.7405 3.9969-4.7405 1.0535 0 1.9314.6919 2.5924.6919.63 0 1.6112-.7333 2.8092-.7333a3.7579 3.7579 0 0 1 3.1604 1.5802zm-3.7284-2.8918a3.5615 3.5615 0 0 0 .8469-2.22 1.5353 1.5353 0 0 0 -.031-.32 3.5686 3.5686 0 0 0 -2.3445 1.2084 3.4629 3.4629 0 0 0 -.8779 2.1585 1.419 1.419 0 0 0 .031.2892 1.19 1.19 0 0 0 .2169.0207 3.0935 3.0935 0 0 0 2.1586-1.1368z"
            ></path>
          </svg>
        </a>
      </li>
      <li v-show="ifShowNavItem" class="nav-items">
        <NavItem
          v-for="(navItem, index) in navItems"
          :key="index"
          :itemText="navItem.itemText"
          :menu="navItem.menu"
          @mouseenter.native="changeNavBarBGC(true)"
          @mouseleave.native="changeNavBarBGC(false)"
          class="nav-item"
        />
      </li>

      <li class="nav-bar-icon serach-icon">
        <a href="https://www.apple.com.cn/search">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="15px"
            height="44px"
            viewBox="0 0 15 44"
          >
            <path
              d="M14.298,27.202l-3.87-3.87c0.701-0.929,1.122-2.081,1.122-3.332c0-3.06-2.489-5.55-5.55-5.55c-3.06,0-5.55,2.49-5.55,5.55 c0,3.061,2.49,5.55,5.55,5.55c1.251,0,2.403-0.421,3.332-1.122l3.87,3.87c0.151,0.151,0.35,0.228,0.548,0.228 s0.396-0.076,0.548-0.228C14.601,27.995,14.601,27.505,14.298,27.202z M1.55,20c0-2.454,1.997-4.45,4.45-4.45 c2.454,0,4.45,1.997,4.45,4.45S8.454,24.45,6,24.45C3.546,24.45,1.55,22.454,1.55,20z"
            ></path>
          </svg>
        </a>
      </li>
      <li class="nav-bar-icon buy-icon">
        <a href="https://www.apple.com.cn/cn/shop/goto/bag">
          <svg
            height="44"
            viewBox="0 0 14 44"
            width="14"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="m11.3535 16.0283h-1.0205a3.4229 3.4229 0 0 0 -3.333-2.9648 3.4229 3.4229 0 0 0 -3.333 2.9648h-1.02a2.1184 2.1184 0 0 0 -2.117 2.1162v7.7155a2.1186 2.1186 0 0 0 2.1162 2.1167h8.707a2.1186 2.1186 0 0 0 2.1168-2.1167v-7.7155a2.1184 2.1184 0 0 0 -2.1165-2.1162zm-4.3535-1.8652a2.3169 2.3169 0 0 1 2.2222 1.8652h-4.4444a2.3169 2.3169 0 0 1 2.2222-1.8652zm5.37 11.6969a1.0182 1.0182 0 0 1 -1.0166 1.0171h-8.7069a1.0182 1.0182 0 0 1 -1.0165-1.0171v-7.7155a1.0178 1.0178 0 0 1 1.0166-1.0166h8.707a1.0178 1.0178 0 0 1 1.0164 1.0166z"
            ></path>
          </svg>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
import NavItem from "./NavItem.vue";
export default {
  name: "NavBar",
  data() {
    return {
      navItems: [
        {
          itemText: "商店",
          menu: [
            {
              groupName: "选购",
              groupSelections: [
                "选购新品",
                "Mac",
                "iPad",
                "iPhone",
                "Apple Watch",
              ],
            },
            {
              groupName: "快速链接",
              groupSelections: [
                "查找零售店",
                "订单状态",
                "分期付款",
                "Apple Trade In 换购计划",
              ],
            },
            {
              groupName: "专属商店选购",
              groupSelections: ["认证的翻新产品", "教育", "商务"],
            },
          ],
        },
        {
          itemText: "Mac",
          menu: [
            {
              groupName: "探索 Mac",
              groupSelections: [
                "探索全部 Mac 机型",
                "MacBook Air",
                "MacBook Pro",
                "iMac",
                "Mac mini",
                "Mac Studio",
                "Mac Pro",
              ],
            },
            {
              groupName: "选购 Mac",
              groupSelections: [
                "选购 Mac",
                "Mac 配件",
                "分期付款",
                "Apple Trade In 换购计划",
              ],
            },
            {
              groupName: "Mac 相关",
              groupSelections: [
                "Mac 支持",
                "macOS Ventura",
                "连续互通",
                "iCloud",
                "Mac 商务应用",
                "教育",
              ],
            },
          ],
        },
        {
          itemText: "iPad",
          menu: [
            {
              groupName: "探索 iPad",
              groupSelections: [
                "探索全部 iPad 机型",
                "iPad Pro",
                "iPad Air",
                "iPad",
                "iPad mini",
                "Apple Pencil",
                "键盘",
              ],
            },
            {
              groupName: "选购 iPad",
              groupSelections: [
                "选购 iPad",
                "iPad 配件",
                "分期付款",
                "Apple Trade In 换购计划",
              ],
            },
            {
              groupName: "iPad 相关",
              groupSelections: ["iPad 支持", "iPadOS 16", "iCloud", "教育"],
            },
          ],
        },

        {
          itemText: "iPhone",
          menu: [
            {
              groupName: "探索 iPhone",
              groupSelections: [
                "探索全部 iPhone 机型",
                "iPhone 14 Pro",
                "iPhone 14",
                "iPhone 13",
                "iPhone 12",
                "iPhone SE",
              ],
            },
            {
              groupName: "选购 iPhone",
              groupSelections: [
                "选购 iPhone",
                "iPhone 配件",
                "Apple Trade In 换购计划",
                "分期付款",
              ],
            },
            {
              groupName: "iPhone 相关",
              groupSelections: [
                "iPhone 支持",
                "iOS 16",
                "iPhone 隐私保护",
                "iCloud",
                "Apple Pay",
                "Siri",
              ],
            },
          ],
        },
      ],
      showNavItem: true,
      baseNavBarClassName: "nav-bar",
      colorNavBarClassName: "nav-bar-bgc1",
    };
  },
  computed: {
    navBarClassName() {
      return this.baseNavBarClassName + " " + this.colorNavBarClassName;
    },
    ifShowNavItem() {
      return this.showNavItem;
    },
  },
  components: {
    NavItem,
  },
  methods: {
    setShowNavItem() {
      const visibleSrceenWidth = document.body.clientWidth;
      if (visibleSrceenWidth < 830) this.showNavItem = false;
      else this.showNavItem = true;
      console.log(visibleSrceenWidth, " | showItem", this.showNavItem);
    },
    changeNavBarBGC(ifEnter) {
      this.colorNavBarClassName = ifEnter ? "nav-bar-bgc2" : "nav-bar-bgc1";
    },
  },
  mounted() {
    this.setShowNavItem();
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.nav-bar {
  height: 48px;
  width: 100%;
  color: #d0d0d1;
  font-size: 12px;
}
.nav-bar-bgc1 {
  background-color: #434344;
}
.nav-bar-bgc2 {
  background-color: #161617;
}
.nav-item:hover {
  cursor: pointer;
}
ul.nav-item-list {
  display: flex;
  justify-content: space-between;
  padding-left: 20px;
  padding-right: 20px;
  height: 100%;
}
li {
  list-style: none;
}
.nav-items {
  width: 100%;
  height: 100%;
  display: contents;
  flex-direction: row;
  justify-content: space-between;
}
.nav-bar-icon svg {
  fill: #d0d0d1;
}
.nav-bar-icon a {
  list-style: none;
}
</style>
