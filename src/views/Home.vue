<template>
  <div class="homeWrap">
    <div class="topnavAndBanner">
      <Topnav />
      <div class="banner">
        <h1>柯基UI</h1>
        <h2>一款 普普通通, 平平无奇 的 UI 框架</h2>
        <p class="actions">
          <a href="https://github.com/simple-ice/crisps-ui">GitHub</a>
          <router-link to="/doc">开始</router-link>
        </p>
      </div>
    </div>
    <div class="features">
      <ul>
        <li>
          <svg class="icon">
            <use xlink:href="#font-dengpao"></use>
          </svg>
          <h3>基于 Vue 3</h3>
          <p>骄傲地使用了 Vue 3 Composition API</p>
        </li>
        <li>
          <svg class="icon">
            <use xlink:href="#font-typescript"></use>
          </svg>
          <h3>基于 TypeScript </h3>
          <p>源代码采用 TypeScript 书写（非严格检查）</p>
        </li>
        <li>
          <svg class="icon">
            <use xlink:href="#font-vuejs-line"></use>
          </svg>
          <h3>代码易读</h3>
          <p>每个组件的源代码都极其简洁</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
import Topnav from "../components/Topnav.vue";
export default {
  name: "Home",
  components: {
    Topnav,
  },
};
</script>

<style lang="scss" scoped>
$bg-pink: #f9bfaf;
$font-color: #bc654c;
$border-radius: 8px;

.homeWrap {
  overflow-y: auto;
}

.features {
  margin: 32px auto 100px;
  padding: 0 30px;

  >ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;

    >li {
      margin: 16px 0;
      display: flex;
      width: 300px;
      padding: 0 40px;
      flex-direction: column;
      align-items: center;
      justify-content: center;

      >svg {
        width: 64px;
        height: 64px;
      }

      >h3 {
        font-size: 1.5em;
      }

      >p {
        text-align: center;
        font-size: 14px;
      }
    }
  }
}

.banner {
  padding: 50px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;

  >h2 {
    margin: 20px 0;
  }

  @media (max-width: 896px) {
    padding-top: 50px + (2.2 * 16px);
  }

  >.actions {
    padding: 8px 0;

    a {
      margin: 0 8px;
      background: $bg-pink;
      display: inline-block;
      color: $font-color;
      padding: 8px 24px;
      border-radius: $border-radius;

      &:hover {
        text-decoration: none;
      }
    }
  }
}
</style>
