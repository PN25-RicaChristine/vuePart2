<template>
  <div id="app">
    <Header
      v-show="$route.name==='register' || $route.name==='login' || $route.name === 'home' ? true : false"
    ></Header>
    <AppBody></AppBody>
    <SidebarMenu
      v-show="$route.name==='dashboard' || $route.name === 'personalinformation' || $route.name === 'courses' || $route.name === 'edit' ? true : false"
    >
      <div slot="header">header</div>
      <div slot="footer">footer</div>
      <span
        class="vsm--toggle-btn"
        :class="{'vsm--toggle-btn_slot' : $slots['toggle-icon']}"
      >toggle-icon</span>
      <span class="dropdown-icon">dropdown-icon</span>
    </SidebarMenu>
  </div>
</template>

<script>
import AUTH from "services/auth";
import Header from "components/frame/Header.vue";
import AppBody from "components/frame/Body.vue";
import SidebarMenu from "components/frame/Sidebar.vue";

export default {
  name: "app",
  auth: AUTH,
  data() {
    return {};
  },
  components: {
    Header,
    AppBody,
    SidebarMenu
  },
  methods: {}
};
</script>

<style>

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  
}

body{
  background-image: url("http://static.asiawebdirect.com/m/phuket/portals/philippines-hotels-ws/homepage/cebu-island/best-cebu-attractions/pagePropertiesImage/best-cebu-attractions.jpg");
  background-size:cover;
}
</style>