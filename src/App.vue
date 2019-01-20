<template>
  <v-app>
    <Banner/>
    <div>
      <v-toolbar color="primary mt-4" dark height="60px">
        <v-toolbar-side-icon class="hidden-md-and-up" @click.stop="drawer = !drawer"></v-toolbar-side-icon>
        <img src="./assets/ASW.png" alt="LOGO" height="80px" style="margin-left:-10px">
        <v-toolbar-items class="hidden-sm-and-down">
          <v-btn id="path" flat router to="/">Timeline</v-btn>
          <v-btn id="path" flat router to="/about">Subbed</v-btn>
          <v-btn id="path" flat>Dubbed</v-btn>
        </v-toolbar-items>
        <v-spacer></v-spacer>
        <v-btn icon>
          <v-icon>search</v-icon>
        </v-btn>
      </v-toolbar>
      <v-navigation-drawer v-model="drawer" temporary absolute width="200">
        <img src="./assets/ASB.png" alt height="100px">
        <v-list class="pt-0" dense>
          <v-divider style="margin-top:-10px"></v-divider>
          <v-list-tile v-for="item in items" :key="item.title" router :to="item.path" id="path">
            <v-list-tile-content>
              <v-list-tile-title>{{ item.title }}</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list>
      </v-navigation-drawer>
    </div>
    <v-content class="ma-4">
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>
import Banner from "./components/Banner";
export default {
  name: "App",
  components: {
    Banner
  },
  data() {
    return {
      drawer: null,
      items: [
        { title: "Timeline", path: "/" },
        { title: "Subbed", path: "/about" },
        { title: "Dubbed", path: "/about" }
      ]
    };
  }
};
</script>

<style>
#path:hover {
  text-decoration: none;
}
</style>