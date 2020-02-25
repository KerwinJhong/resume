<template>
  <v-container>
    <v-row>
      <v-col
        v-for="(item, index1) in projects"
        :key="index1"
        cols="12"
        sm="6"
        md="4"
      >
        <v-card max-width="344" class="mx-auto">
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title class="headline">
                Our Changing Planet
              </v-list-item-title>
              <v-list-item-subtitle>by Kurt Wagner</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
          <v-img src="https://cdn.vuetifyjs.com/images/cards/mountain.jpg" height="194"></v-img>
          <v-card-text>
            Visit ten places on our planet that are undergoing the biggest changes today.
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn icon>
              <v-icon>mdi-application</v-icon>
            </v-btn>
            <v-btn icon>
              <v-icon>mdi-git</v-icon>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      projects: [
        {
          title: 'frontend',
          items: [
            { name: 'vue', icon: 'mdi-vuejs' },
            { name: 'nuxt', icon: 'mdi-nuxt' },
            { name: 'vuetify', icon: 'mdi-vuetify' }
          ]
        }, {
          title: 'backend',
          items: [
            { name: 'node', icon: 'mdi-nodejs' },
            { name: 'express', icon: 'mdi-tools' },
            { name: 'sequelize', icon: 'mdi-tools' },
            { name: 'mongoose', icon: 'mdi-tools' }
          ]
        }, {
          title: 'others',
          items: [
            { name: 'git', icon: 'git' },
            { name: 'git flow', icon: 'mdi-tools' },
            { name: 'trello', icon: 'mdi-trello' },
            { name: 'hackmd', icon: 'mdi-tools' },
            { name: 'balsamiq mockups 3', icon: 'mdi-lead-pencil' },
            { name: 'heroku', icon: 'mdi-tools' }
          ]
        }
      ]
    }
  }
}
</script>
