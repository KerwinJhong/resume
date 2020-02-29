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
          <v-col
            v-for="(item, index1) in skill.items"
            :key="index1"
            class="text-center"
            cols="6"
            xs="6"
            sm="4"
            md="2"
          >
            <v-hover>
              <template v-slot="{ hover }">
                <v-card class="mx-auto py-3" max-width="1100" :elevation="hover ? 24 : 6">
                  <v-icon v-if="item.icon" x-large :style="`color: ${item.color};`">
                    {{ item.icon }}
                  </v-icon>
                  <v-img
                    v-else
                    eager
                    class="mx-auto"
                    height="40"
                    width="40"
                    :src="item.img"
                    :lazy-src="item.img"
                  />
                  <v-list-item-title class="text-capitalize mt-2">
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
            { name: 'socket.IO', img: require('@/assets/socket.png'), color: '#757575' },
            { name: 'bootstrap 4', img: require('@/assets/Bootstrap.png'), color: '#CD6799' }
          ]
        }, {
          title: 'backend',
          items: [
            { name: 'node', icon: 'mdi-nodejs', color: '#95B94D' },
            { name: 'express', icon: 'mdi-tools', color: '#757575' },
            { name: 'sequelize', img: require('@/assets/sequelize.png'), color: '#757575' },
            { name: 'mongoose', icon: 'mdi-tools', color: '#757575' }
          ]
        }, {
          title: 'others',
          items: [
            { name: 'git', icon: 'git', color: '#E94E32' },
            { name: 'git flow', icon: 'mdi-tools', color: '#757575' },
            { name: 'heroku', img: require('@/assets/heroku.png'), color: '#757575' },
            { name: 'netlify', img: require('@/assets/netlify.png'), color: '#757575' },
            { name: 'mySQL Workbench', img: require('@/assets/MySQL Workbench.png'), color: '#757575' },
            { name: 'mongod', img: require('@/assets/mongod.png'), color: '#757575' },
            { name: 'postman', img: require('@/assets/postman.png'), color: '#757575' },
            { name: 'balsamiq mockups', img: require('@/assets/Balsamiq Mockups 3.png'), color: '#757575' },
            { name: 'trello', icon: 'mdi-trello', color: '#007CC3' },
            { name: 'hackmd', icon: 'mdi-file-document', color: '#757575' }
          ]
        }
      ]
    }
  }
}
</script>
