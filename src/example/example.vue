<template>
  <div id="app">
    <div class="demo-header">
      <img class="log-img" src="../assets/images/logo.gif" alt="">
      <div class="logo">云集前端Demo</div>
    </div>
    <ul class="demo-sidebar">
      <li class="sidebar-item" v-for="(item, index) in RouterConfig" :key="index">
        <router-link :to="item">{{item.meta.title}}</router-link>
      </li>
    </ul>
    <div class="demo-content">
      <div class="demo-wrapper">
        <router-view></router-view>
      </div>
    </div>
  </div>
</template>

<script>
  import RouterConfig from '../router/router.config';

  export default {
    data() {
      return {
        RouterConfig
      };
    },
    methods: {
      directUrl(item) {
        this.$router.push(item);
      }
    }
  };
</script>

<style lang="less">
  .demo-header {
    position: fixed;
    display: flex;
    align-items: center;
    top: 0;
    height: 60px;
    width: 100%;
    color: white;
    padding: 0px 60px;
    background-color: rgb(32, 160, 255);

    .logo {
      font-size: 22px;
      display: flex;
      fldemo-direction: row;
      align-item: center;

    }
    .log-img {
      width: 50px;
      height: 35px;
    }
  }

  .demo-sidebar {
    position: fixed;
    width: 220px;
    height: calc(~'100% - 61px');
    top: 61px;
    left: 0;
    overflow-y: auto;

    .sidebar-item {

      a {
        display: block;
        height: 40px;
        line-height: 40px;
        font-size: 13px;
        padding-left: 24px;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;

        &.router-link-active {
          color: #20a0ff;
        }
      }
    }
  }

  .demo-content {
    padding-left: 220px;
    padding-top: 61px;
    height: 100%;

    .demo-wrapper {
      padding: 20px;
      height: 100%;
      overflow: auto;
      background-color: white;
    }
  }
</style>
