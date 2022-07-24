<template>
  <v-container pt-5>
    <v-card-title class="text-h4 justify-center">これまでの人生</v-card-title>
    <v-timeline dense>
      <v-timeline-item
        v-for="myHistoryTitle in myHistoryTitles"
        :key="myHistoryTitle"
        large
        class="pt-5"
      >
        <template v-slot:icon>
          <v-avatar>
            <img :src="myHistoryTitle.picture" />
          </v-avatar>
        </template>

        <v-card class="elevation-2">
          <v-card-text>{{ myHistoryTitle.title }} </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'

@Component
export default class TimeLine extends Vue {
  myHistoryTitles = [
    {
      picture: '/Udon.jpg',
      title: 'うどん県にて誕生、夢は化学者になることだった',
    },
    {
      picture: 'Ryouma.jpg',
      title: '小学6年、龍馬県に引越し',
    },
    {
      picture: '/NotGoSchool.png',
      title: '高校受験など日々忙しく、体調を壊し不登校になった',
    },
    { picture: 'Miku.jpg', title: '初音ミクと運命の出会いを果たし、心が回復' },
    { picture: 'MikuMiku.jpg', title: '部屋が初音ミクで埋まっていく' },
    {
      picture: 'Mikan.jpg',
      title: 'みかん県に引越し、新天地で馴染めず高校に行かない日が増えた',
    },
    {
      picture: 'Gold.jpg',
      title: '人生で初めて髪を染める',
    },
    { picture: 'Music.jpg', title: '楽譜も読めない状態で合唱部に入団' },
    { picture: 'Suite.jpg', title: '社会人に' },
    { picture: 'Ill.png', title: '病気により即退社' },
    { picture: 'Pc.jpg', title: 'IT業界へ' },
    { picture: 'Mirai.jpg', title: '初めてマジカルミライに参戦' },
    { picture: 'Study.jpg', title: '日々勉強' },
  ]
}
</script>
