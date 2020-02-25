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
                  <v-icon x-large class="mb-2">
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
