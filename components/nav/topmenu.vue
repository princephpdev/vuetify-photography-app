<template>
    <div>
      <v-app-bar flat dark>
        <v-toolbar-title>Var Yatra</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn text :to="link.url" v-for="link in links" :key="link.title" class="hidden-sm-and-down" nuxt>
          {{link.title}}
        </v-btn>
        <v-app-bar-nav-icon class="hidden-md-and-up" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
    </v-app-bar>
    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
      dark
    >
      <v-list>

        <v-list-item
          v-for="link in links"
          :key="link.title"
          link
          :to="link.url"
        >
          <v-list-item-content>
            <v-list-item-title :to="link.url">{{ link.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    </div>
</template>

<script>
export default {
  data() {
    return {
      links : [
      {
        title: 'Home',
        url : '/',
      },
      {
        title: 'About',
        url : '/about',
      },
      {
        title : 'Gallery',
        url : '/gallery',
      },
      {
        title : 'Films',
        url : '/films',
      },
      {
        title : 'Contact',
        url : '/contact',
      }
      ],
    drawer: null,
     }
  }
}
</script>