<template>
  <header class="header">
    <div class="logo-area">
      <p>自己点検システム</p>
    </div>
    <div class="menu-area">
      <div class="menu-toggle">
        <i v-if="!showMenu" class="fa fa-angle-down" @click="menuToggle()"/>
        <i v-else class="fa fa-angle-up" @click="menuToggle()"/>
      </div>
      <div :class="{show: showMenu, none: !showMenu}" class="menu-blocks">
        <div class="menu-block sp-only-show" @click="menuToggle()">
          <nuxt-link to="/" tag="a">
            TOPへ
          </nuxt-link>
        </div>
        <div class="menu-block" @click="menuToggle()">
          <nuxt-link to="/timeline" tag="a">
            タイムライン
          </nuxt-link>
        </div>
        <div class="menu-block" @click="menuToggle()">
          <nuxt-link to="/egos" tag="a">
            ego
          </nuxt-link>
        </div>
        <div class="menu-block" @click="menuToggle()">
          <nuxt-link to="/message" tag="a">
            メッセージ
          </nuxt-link>
        </div>
        <div class="menu-block" @click="menuToggle()">
          <nuxt-link to="/dashboard" tag="a">
            ダッシュボード
          </nuxt-link>
        </div>
        <div class="menu-block" @click="menuToggle()">
          <nuxt-link to="/egos/create" tag="a">
            ego新規登録
          </nuxt-link>
        </div>
        <div class="menu-block" @click="menuToggle()">
          <nuxt-link to="/diaries/create" tag="a">
            日記登録
          </nuxt-link>
        </div>
        <div class="menu-block" @click="menuToggle()">
          <vs-avatar vs-src="https://avatars2.githubusercontent.com/u/31676496?s=460&v=4"/>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      showMenu: false
    }
  },
  methods: {
    menuToggle() {
      this.showMenu = !this.showMenu
    }
  }
}
</script>

<style lang="scss" scoped>
.header {
   position: fixed;
   top: 0;
   left: 0;
   width: 100%;
   height: 60px;
   z-index: 2;
   border-bottom: $border-color 1px solid;
   padding: 20px;
   background-color: #fff;
   display: flex;
   justify-content: center;
   align-items: center;
   .logo-area {
     flex: 1;
     .logo {
       height: 40px;
     }
   }
   .menu-area {
     @include mq(sm) {
       flex: 5;
     }
     @include mq() {
       flex: 8;
     }
     .menu-blocks {
       @include mq(sm) {
         position: absolute;
         top: 60px;
         left: 0;
         width: 100%;
         background-color: #fff;
         &.show {
           display: block;
         }
         &.none {
           display: none;
         }
       }
       @include mq() {
         display: flex;
         justify-content: flex-end;
         align-items: center;
       }
       .menu-block {
         padding: 10px 20px;
       }
     }
     .menu-toggle {
       @include mq(sm) {
         padding-left: 10px;
         font-size: 1.5em;
       }
       @include mq() {
         display: none;
       }
     }
   }
 }
</style>
