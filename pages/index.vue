<template>
  <v-container>
    <!-- 後ろでミクを踊らせる。 unityで作成したものを動画にして背景として利用 ボタンで背景で踊るミクを変更可能-->
    <v-row> <TopTheme :profile="profile" /> </v-row>

    <v-container>
      <v-row>
        <v-col cols="12" align="center" class="text-h4">スキル</v-col>
      </v-row>
      <v-row>
        <v-col>
          <MyJobAbilityChart />
        </v-col>
        <v-col>
          <MyInterstAbilityChart />
        </v-col>
        <v-col>
          <MyHobbyAbilityChart />
        </v-col>
      </v-row>
      <v-row>
        <v-card></v-card>
      </v-row>
      <TimeLine />
    </v-container>
    <ContactWay />
  </v-container>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'
import TopTheme from '~/components/TopTheme.vue'
import FaceLogo from '~/components/FaceLogo.vue'
import TimeLine from '~/components/TimeLine.vue'
import MyJobAbilityChart from '~/components/MyJobAbilityChart.vue'
import MyInterstAbilityChart from '~/components/MyInterestAbilityChart.vue'
import MyHobbyAbilityChart from '~/components/MyHobbyAbilityChart.vue'
import ContactWay from '~/components/ContactWay.vue'

@Component({
  components: {
    FaceLogo,
    TopTheme,
    TimeLine,
    MyJobAbilityChart,
    MyInterstAbilityChart,
    MyHobbyAbilityChart,
    ContactWay,
  },
})
export default class IndexPage extends Vue {
  profile = {
    myName: "TAKIGAWA's profile",
    hobby: 'ゲーム',
    country: '日本',
  }
}
</script>
