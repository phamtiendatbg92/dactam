<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      disable-resize-watcher
      :mini-variant="miniVariant"
      class="d-lg-none"
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="d-lg-none"/>
      <router-link to="/">
        <v-img src="/logo-icon.png" max-height="40" max-width="40" contain />
      </router-link>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-btn router to="/" class="d-none d-sm-flex">Home</v-btn>
      <v-btn router to="/cong-tac-vien" class="d-none d-sm-flex">Cộng Tác Viên</v-btn>
      <v-btn router to="/san-pham" class="d-none d-sm-flex">Sản phẩm</v-btn>
      <v-btn router to="/lien-he" class="d-none d-sm-flex">Liên hệ</v-btn>
      <!--spacer is used for put an icon in right side-->
      <v-spacer />
      <v-btn icon @click.stop="">
        <v-icon>mdi-cart</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container fluid>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/",
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire",
        },
      ],
      miniVariant: false,
      title: "Tinh Hoa Dược Liệu Việt",
    };
  },
  computed:{
    isShowDraw: function(){
      //alert("change");
      return this.drawer;
    }
  },
  method:{
    onCartClick(){
      alert("cart click");
    }
  }
};
</script>

<style scoped>
</style>