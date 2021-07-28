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
      <v-app-bar-nav-icon
        @click.stop="drawer = !drawer"
        class="d-flex d-md-none"
      />
      <router-link to="/">
        <v-img src="/logo-icon.png" max-height="40" max-width="40" contain />
      </router-link>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-btn router to="/" class="d-none d-md-flex">Home</v-btn>
      <v-btn router to="/cong-tac-vien" class="d-none d-md-flex"
        >Cộng Tác Viên</v-btn
      >
      <v-btn router to="/san-pham" class="d-none d-md-flex">Sản phẩm</v-btn>
      <v-btn router to="/lien-he" class="d-none d-md-flex">Liên hệ</v-btn>
      <v-spacer />
      <v-btn icon @click.stop="">
        <v-icon>mdi-cart</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container fluid class="px-md-10 px-lg-16">
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="!fixed" app>
      <v-container fluid class="px-md-10 px-lg-16">
        <v-row>
          <v-col cols="4">
            <v-card>
              <v-card-title class="display-1">DƯỢC LIỆU ĐẮC TÂM</v-card-title>
              <v-card-subtitle class="font-weight-bold">
                <v-icon>mdi-storefront-outline</v-icon> Kho
                hàng:</v-card-subtitle
              >
              <v-card-text>
                <strong> ★ Hà Nội: </strong> 225 đường Quan Hoa, quận Cầu Giấy,
                TP.Hà Nội.
                <br />
                <strong> ★ Sài Gòn: </strong> B3 chung cư Hoàng Anh Gold House, 187
                Lê Văn Lương, Phước Kiển, Nhà Bè, TP.HCM.
                <br />
                <strong> ★ Bắc Giang: </strong> số 243, đường Lê Lợi, TP.Bắc Giang.
              </v-card-text>

              <v-card-subtitle class="font-weight-bold">
                <v-icon>mdi-phone</v-icon> SĐT: <span class="font-weight-regular">0854.277.626</span> 
                </v-card-subtitle>
              <v-card-subtitle class="font-weight-bold">
                <v-icon>mdi-card-account-mail</v-icon> Giờ làm việc: <span class="font-weight-regular">9h – 21h tất cả các ngày trong tuần.</span>
                </v-card-subtitle
              >
            </v-card>
          </v-col>
        </v-row>
      </v-container>
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
  computed: {
    isShowDraw: function () {
      //alert("change");
      return this.drawer;
    },
  },
  method: {
    onCartClick() {
      alert("cart click");
    },
  },
};
</script>

<style scoped>
</style>