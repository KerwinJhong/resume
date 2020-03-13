<template>
  <div>
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
              Hi, 我是 Kerwin，在機械業有兩年製程工程師經驗，專門幫助企業解決製程上的機械問題，不僅在細節中發現問題，也在問題中發現細節，習慣與問題共存。
            </p>
            <p class="text-justify">
              在學與工作時都有學到程式相關經驗，也漸漸對程式有興趣，在閒暇時間了解程式相關工作後，開始在 W3Schools 刷題目練習，之後在程式中有些基礎後決定踏入相關課程。
            </p>
            <p class="text-justify">
              在2019年七月加入 ALPHA Camp 開始為期八個月的全端學習，過程中相當喜歡團體協作的氛圍，也在最後期間將所學的技術與組員一同完成CRM專案，在專案中獨立擔任前端工程師。
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
    <Waves />
  </div>
</template>

<script>
import Waves from '@/components/Waves.vue'
export default {
  components: {
    Waves
  },
  data () {
    return {
      name: '鐘顯宗(Kerwin Jhong)'
    }
  }
}
</script>
