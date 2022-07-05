<template>
  <v-container>
    <v-row>
      <FaceLogo :myName="profile" />
    </v-row>
    <v-row>
      <v-card width="80%" height="auto" class="mx-auto my-3 rounded-xl">
        <v-row>
          <v-col cols="4" align="center">
            <h2>スキル</h2>
            <v-list>
              <v-list-item>
                <v-list-item-content>
                  <v-list-item-title>言語:JS,PHP,Python</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
            <v-list>
              <v-list-item>
                <v-list-item-content>
                  <v-list-item-title>
                    DB:oracle,postgresql,mariadb</v-list-item-title
                  >
                </v-list-item-content>
              </v-list-item>
            </v-list>
            <v-list>
              <v-list-item>
                <v-list-item-content>
                  <v-list-item-title> クラウド:GCP</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
            <v-list>
              <v-list-item>
                <v-list-item-content>
                  <v-list-item-title> ver管理:svn,git</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>
        </v-row>
      </v-card>
    </v-row>
    <v-row>
      <v-card width="80%" height="auto" class="mx-auto my-3 rounded-xl">
        <v-row>
          <v-col cols="4" align="center">
            <h2>My Intro</h2>
            <ul style="list-style: none">
              <li>あだ名</li>
              <p>タッキー</p>
              <li>座右の銘</li>
              <p>朝日は登らない</p>
              <li>必殺技</li>
              <p>寝る</p>
            </ul></v-col
          >
        </v-row>
      </v-card>
    </v-row>
  </v-container>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'
import FaceLogo from '~/components/FaceLogo.vue'

@Component({
  components: {
    FaceLogo,
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
