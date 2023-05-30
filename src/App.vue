<template>
  <div id="app">
    <nav-bar />
    <!-- <aside-menu :menu="menu" />
     -->
    <VueSidebarMenuAkahon />
    <router-view />
    <footer-bar />
  </div>
</template>

<script>
import { defineComponent } from 'vue'
import menu from '@/menu.js'
import NavBar from '@/components/NavBar.vue'
// import AsideMenu from '@/components/AsideMenu.vue'
import FooterBar from '@/components/FooterBar.vue'
import VueSidebarMenuAkahon from 'vue-sidebar-menu-akahon'
export default defineComponent({
  name: 'AppComponent',
  components: {
    FooterBar,
    // AsideMenu,
    VueSidebarMenuAkahon,
    NavBar
  },
  data () {
    return {
      menu
    }
  },
  created () {
    this.$store.commit('user', {
      name: 'John Doe',
      email: 'john@example.com',
      avatar: 'https://avatars.dicebear.com/v2/gridy/John-Doe.svg'
    })
  }
})
</script>
