<template>
  <div id="app">
    <template comments>
      <div>
        <!-- comments -->
      </div>
    </template>
    <TopBar title="XING博客" :logo="require('@/assets/logo.webp')" class="topbar">
      <template #list>
        <div class="list">
          <ul>
            <router-link to="/">
              <!-- <a href="/"> -->
              <li>首页</li>
              <!-- </a> -->
            </router-link>
            <router-link to="/add">
              <!-- <a href="/index"> -->
              <li>投稿</li>
              <!-- </a> -->
            </router-link>
          </ul>
        </div>
      </template>
    </TopBar>
    <router-view></router-view>
    <BottomInfo></BottomInfo>
  </div>
</template>

<script>
import TopBar from '@/components/topBar.vue'
// import logo from '@/assets/logo.png'
import BottomInfo from '@/components/bottomInfo.vue'
export default {
  components: { TopBar, BottomInfo },
  data() {
    return {
      // logo
    }
  }
}
</script>

<style lang="less">
.content {
  // height: 100%;
  padding-top: 66px;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  color: #2c3e50;
  background-color: #eee;
  // height: 100vh;
  width: 100%;
  .topbar {
    position: fixed;
    z-index: 100;
    width: 100%;
  }
  .list {
    // position: absolute;
    // right: 0;
    margin-left: 40px;
    ul {
      width: 140px;
      display: flex;
      justify-content: space-between;
      flex-wrap: nowrap;
      li {
        padding: 0 10px;
        font-size: 16px;
        flex-wrap: nowrap;
        color: #111;
        &:hover {
          color: #42b983;
        }
      }
    }
  }
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
