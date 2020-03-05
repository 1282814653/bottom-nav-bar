# 导航栏

```html
<template>
  <div id="app" class="app-main">
    <router-view />
    <div class="footer-bar">
      <router-link class="router-link home" to="/home"></router-link>
      <router-link class="router-link movie" to="/movie"></router-link>
      <router-link class="router-link ticket" to="/ticket"></router-link>
      <router-link class="router-link cinema" to="/cinema"></router-link>
      <router-link class="router-link main" to="/main"></router-link>
    </div>
  </div>
</template>

<style lang="scss">
html,
body {
  height: 100%;
}
a {
  -webkit-tap-highlight-color: transparent;
}
</style>

<style lang="scss" scoped>
.app-main {
  .footer-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: fixed;
    left: 0;
    bottom: 0;
    height: 105px;
    width: 100%;
    background-image: url("../src/assets/imgs/icons/icon-footer-bg.png");
    background-size: 100% 100%;
    .router-link {
      width: 72px;
      height: 72px;
      background-color: orange;
      background: no-repeat center;
      background-size: 44px 44px;
      margin-top: 32px;
      &.home {
        background-image: url("../src/assets/imgs/icons/icon-home.png");
        &.router-link-active {
          background-image: url("../src/assets/imgs/icons/icon-home-active.png");
        }
      }
      &.ticket {
        background-image: url("../src/assets/imgs/icons/icon-ticket.png");
        background-size: 70px 70px;
        margin-top: -1px;
      }
      &.cinema {
        background-image: url("../src/assets/imgs/icons/icon-cinema.png");
        &.router-link-active {
          background-image: url("../src/assets/imgs/icons/icon-cinema-active.png");
        }
      }
      &.movie {
        background-image: url("../src/assets/imgs/icons/icon-movie.png");
        &.router-link-active {
          background-image: url("../src/assets/imgs/icons/icon-movie-active.png");
        }
      }
      &.main {
        background-image: url("../src/assets/imgs/icons/icon-main.png");
        &.router-link-active {
          background-image: url("../src/assets/imgs/icons/icon-main-active.png");
        }
      }
    }
  }
}
</style>

```