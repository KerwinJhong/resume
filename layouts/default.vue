<template>
  <v-app light>
    <v-navigation-drawer v-model="drawer" :mini-variant="miniVariant" app>
      <v-list>
        <v-list-item v-for="(item, i) in items" :key="i" :to="item.to" router exact>
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar class="cyan accent-3" app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-toolbar-title>
        Kerwin's Resume
      </v-toolbar-title>
      <a href="https://medium.com/@sh940718" style="width: 48px;" target="_blank">
        <v-img
          height="24"
          width="24"
          class="mx-auto"
          style="border-radius: 50%;"
          :src="require('@/assets/Medium icon.png')"
        />
      </a>
      <v-btn
        icon
        href="https://www.facebook.com/people/%E9%90%98%E9%A1%AF%E5%AE%97/100008406492174"
        target="_blank"
      >
        <v-icon style="color: black;">
          mdi-facebook
        </v-icon>
      </v-btn>
    </v-app-bar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer class="cyan accent-3" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-triforce',
          title: 'Project',
          to: '/project'
        },
        {
          icon: 'mdi-tools',
          title: 'Skills',
          to: '/skills'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false
    }
  }
}
</script>
