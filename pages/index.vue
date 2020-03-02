<template>
  <v-card class="mx-auto" max-width="1100" outlined>
    <v-container>
      <v-row>
        <v-col class="text-center" cols="12" md="2">
          <v-img eager max-width="150" :src="require('@/assets/avatar.jpg')" :lazy-src="require('@/assets/avatar.jpg')"></v-img>
        </v-col>
        <v-col cols="12" md="10">
          <h4 class="title font-weight-black mb-2">
            {{ name }}
          </h4>
          <p class="text-justify">
            {{ text }}
          </p>
          <p class="pb-1">
            <v-icon class="mr-2">
              mdi-email-mark-as-unread
            </v-icon>Email&#65306;sh940718@gmail.com
          </p>
          <p>
            <v-icon class="mr-2">
              mdi-map-marker
            </v-icon>Address&#65306;高雄市三民區
          </p>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
export default {
  data () {
    return {
      name: '鐘顯宗(Kerwin Jhong)',
      text: 'Hi,我是 Kerwin ，在2019年七月加入 ALPHA Camp 開始為期七個月的學習，過程中相當喜歡團體協作、相互激勵、一同成長的氛圍，在最後期間將所學的技術與組員一同完成CRM專案，所以開始尋找前端工程師的職務。'
    }
  }
}
</script>
