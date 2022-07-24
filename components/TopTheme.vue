<template>
  <v-container>
    <v-row>
      <v-col cols="6" align="right" class="mr-3">
        <v-img src="/my-face.png" class="my-face rounded-circle"> </v-img>
      </v-col>
      <v-col>
        <h3>{{ profile.myName }}</h3>
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>趣味:{{ profile.hobby }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title
                >出身国:{{ profile.country }}</v-list-item-title
              >
            </v-list-item-content>
          </v-list-item>
        </v-list>
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                Link:<a href="https://github.com/0t3k25">GitHub</a>
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'nuxt-property-decorator'

@Component
export default class FaceLogo extends Vue {
  @Prop(Object) readonly profile: any
}
</script>

<style>
.my-face {
  width: 200px;
}
</style>
