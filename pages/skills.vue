<template>
  <v-container>
    <v-breadcrumbs :items="items" large>
      <template v-slot:item="{ item }">
        <v-breadcrumbs-item :href="`#${item}`" class="text-capitalize">
          {{ item }}
        </v-breadcrumbs-item>
      </template>
    </v-breadcrumbs>
    <v-card v-for="(skill, index) in skills" :key="index" class="mx-auto mb-4" max-width="1100" outlined>
      <v-list-item-content class="px-5">
        <v-list-item-title :id="skill.title" class="headline text-capitalize">
          {{ skill.title }}
        </v-list-item-title>
        <v-row>
          <v-col v-for="(item, index1) in skill.items" :key="index1" class="text-center" cols="4" md="2">
            <v-hover>
              <template v-slot="{ hover }">
                <v-card class="mx-auto py-3" max-width="1100" :elevation="hover ? 24 : 6">
                  <v-icon x-large class="mb-2" :style="`color: ${item.color};`">
                    {{ item.icon }}
                  </v-icon>
                  <v-list-item-title class="text-capitalize">
                    {{ item.name }}
                  </v-list-item-title>
                </v-card>
              </template>
            </v-hover>
          </v-col>
        </v-row>
      </v-list-item-content>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      items: ['frontend', 'backend', 'others'],
      skills: [
        {
          title: 'frontend',
          items: [
            { name: 'vue', icon: 'mdi-vuejs', color: '#42B983' },
            { name: 'nuxt', icon: 'mdi-nuxt', color: '#42B983' },
            { name: 'vuetify', icon: 'mdi-vuetify', color: '#AEDDFF' },
            { name: 'scss', icon: 'mdi-sass', color: '#CD6799' },
            { name: 'socket.IO', icon: 'mdi-tools', color: '#757575' }
          ]
        }, {
          title: 'backend',
          items: [
            { name: 'node', icon: 'mdi-nodejs', color: '#95B94D' },
            { name: 'express', icon: 'mdi-tools', color: '#757575' },
            { name: 'sequelize', icon: 'mdi-tools', color: '#757575' },
            { name: 'mongoose', icon: 'mdi-tools', color: '#757575' }
          ]
        }, {
          title: 'others',
          items: [
            { name: 'git', icon: 'git', color: '#E94E32' },
            { name: 'git flow', icon: 'mdi-tools', color: '#757575' },
            { name: 'trello', icon: 'mdi-trello', color: '#007CC3' },
            { name: 'hackmd', icon: 'mdi-tools', color: '#757575' },
            { name: 'balsamiq mockups 3', icon: 'mdi-tools', color: '#757575' },
            { name: 'heroku', icon: 'mdi-tools', color: '#757575' }
          ]
        }
      ]
    }
  }
}
</script>
