<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
          color="red darken-4"
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
    <v-app-bar :clipped-left="clipped" fixed app color="red darken-4">
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon>mdi-{{ `chevron-${miniVariant ? "right" : "left"}` }}</v-icon>
      </v-btn>
      <v-btn icon @click.stop="clipped = !clipped">
        <v-icon>mdi-application</v-icon>
      </v-btn>
      <!-- <v-btn icon @click.stop="fixed = !fixed">
        <v-icon>mdi-minus</v-icon>
      </v-btn> -->
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <!-- <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-menu</v-icon>
      </v-btn> -->
    </v-app-bar>
    <v-main>
      <!-- <v-container> -->
      <nuxt />
      <!-- </v-container> -->
    </v-main>
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light> mdi-repeat </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer color="red darken-4 lighten-1" padless>
      <v-row justify="center" no-gutters>
        <v-btn
          v-for="(link,i) in links"
          :key="i"
          color="white"
          text
          rounded
          class="my-2"
          :to="link.to"
        >
          {{ link.title }}
        </v-btn>
        <v-col class="black lighten-2 py-4 text-center white--text" cols="12">
            <small>〒790-0003松山市三番町1-10-22</small>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      //サイドメニューバー
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          title: "Home",
          to: "/",
        },
        {
          title: "Menu",
          to: "/menu",
        },
        {
          title: "Access",
          to: "#a",
        },
      ],
      //フッターメニューバー
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "",
      links: [
        {
          title: "Home",
          to: "/",
        },
        {
          title: "Menu",
          to: "/menu",
        },
        {
          title: "Access",
          to: "#a",
        },
      ],
    };
  },
};
</script>

<style>
img {
  width: 60%;
  margin: 10px 54px 10px 54px;
}
</style>