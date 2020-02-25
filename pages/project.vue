<template>
  <v-container>
    <v-row>
      <v-col
        v-for="(item, index) in projects"
        :key="index"
        cols="12"
        sm="6"
        md="4"
      >
        <v-card max-width="344" class="mx-auto">
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title class="headline">
                {{ item.title }}
              </v-list-item-title>
              <v-list-item-subtitle>{{ item.skills }}</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
          <v-img eager height="194" :src="item.img" :lazy-src="item.img"></v-img>
          <v-chip v-for="(chip, index1) in item.items" :key="index1" class="ma-2" color="primary">
            {{ chip }}
          </v-chip>
          <v-divider class="mx-4"></v-divider>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn icon :href="item.heroku" target="_blank">
              <v-icon>mdi-application</v-icon>
            </v-btn>
            <v-btn icon :href="item.github" target="_blank">
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
          title: 'CRM-濾客平台',
          skills: 'vue、vuex、scss',
          img: require('@/assets/CRM.png'),
          items: ['獨立開發', '與後端工程師共同開發', 'wireframe', 'POS功能', 'Dashboard', '客戶端-點餐功能', '開發時程6週'],
          heroku: 'https://recus.herokuapp.com/signin',
          github: 'https://github.com/IgnacioFan/recus-platform'
        }
      ]
    }
  }
}
</script>
