<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">App Name</div>

      <v-spacer></v-spacer>
      <drop-down-menu :menu-items="menuItems" />
    </v-app-bar>

    <v-content>
      <router-view />
    </v-content>
    <v-bottom-navigation
      class="b_container"
      v-model="bottomNav"
      fixed
      bottom
      background-color="primary"
    >
      <v-btn value="recent">
        <span>Recent</span>
        <v-icon>mdi-history</v-icon>
      </v-btn>

      <v-btn value="favorites">
        <span>Favorites</span>
        <v-icon>mdi-heart</v-icon>
      </v-btn>
      <v-btn value="favorites">
        <span>Favorites</span>
        <v-icon>mdi-heart</v-icon>
      </v-btn>
      <v-btn value="favorites">
        <span>Favorites</span>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn value="nearby">
        <span>Nearby</span>
        <v-icon>mdi-map-marker</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </v-app>
</template>

<script>
import DropDownMenu from "@/components/widgets/DropDownMenu";
export default {
  name: "App",
  components: {
    DropDownMenu
  },
  data: () => ({
    bottomNav: null,
    menuItems: [
      {
        name: "Setting",
        link: "/settings"
      },
      {
        name: "Logout",
        link: "/logout"
      }
    ]
  })
};
</script>
<style scoped>
.b_container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
