<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :clipped="clipped"
      fixed
      app
      temporary
    >
      <v-app-bar color="deep-purple darken-4" dark>
        <v-toolbar-title v-text="menuTitle" class="white--text" />
      </v-app-bar>
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
    <v-content>
      <div class="app-content">
        <nuxt />
      </div>
    </v-content>
    <v-navigation-drawer :right="right" temporary fixed> </v-navigation-drawer>
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
          title: "Home",
          to: "/"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Contact",
          to: "/inspire"
        }
      ],
      miniVariant: false,
      right: true,
      title: "Team Bouesso",
      menuTitle: "Menu"
    };
  }
};
</script>
<style>
* {
  box-sizing: border-box;
}
@font-face {
  font-family: "ZilapAfrica";
  font-weight: normal;
  src: url("~assets/fonts/ZilapAfrica.ttf") format("ttf");
}
@font-face {
  font-family: "zilap-afro-demo";
}
body {
  font-family: "zilap-afro-demo", truetype;
  background: linear-gradient(rgba(to right bottom, red, yellow, green, 0.7))
    transparent;
  margin: 0;
  padding: 0;
}
.v-toolbar__title {
  background: -webkit-linear-gradient(
    to right,
    #ffb347,
    #fd1d1d,
    #fcb045
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #ffb347,
    #fd1d1d,
    #fcb045
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-family: "ZilapAfrica";
}
body > * {
  white-space: pre-line;
}
.app-content {
  margin-top: 0;
}
@font-face {
  font-family: "zilap-afro-demo";
  src: url("~assets/fonts/ZilapAfroDemo.ttf") format("truetype");
}
span.font1 {
  font-family: "zilap-afro-demo";
  font-size: 55px;
  text-transform: none;
}
h1,
h2 {
  background-image: linear-gradient(
    rgba(to right bottom, red, yellow, green, 0.7)
  );
}
.toolbar {
  font-family: "zilap-afro-demo";
  font-size: 200%;
}
.navigation {
  top: 0; /* Stay on top */
  transition: top 0.3s;
  background-color: transparent;
}
</style>
