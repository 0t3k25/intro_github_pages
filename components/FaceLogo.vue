<template>
  <v-card width="80%" height="auto" class="rounded-xl mx-auto">
    <!-- <v-row no-gutters>
      <v-col :cols="3">
        <v-card class="pa-2" outlined tile> col-3 </v-card>
        
      </v-col>
      <v-col :cols="9" :md="4">
        <v-card class="pa-2" outlined tile> col-9 </v-card>
        <v-card-text>{{ $attrs.name }}</v-card-text>
      </v-col> -->
    <!-- </v-row> -->
    <v-row no-gutters align-content="center">
      <v-col cols="4" align="center" class="py-5">
        <h3>{{ $attrs.myName['myName'] }}</h3>
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title
                >趣味:{{ $attrs.myName['hobby'] }}</v-list-item-title
              >
            </v-list-item-content>
          </v-list-item>
        </v-list>
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title
                >出身国:{{ $attrs.myName['country'] }}</v-list-item-title
              >
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-col>
      <v-col align="center" cols="8">
        <v-img src="/my-face.png" class="my-5 my-face rounded-circle"> </v-img>
      </v-col>
    </v-row>
  </v-card>
</template>

<script lang="ts">
import { Vue, Prop } from 'nuxt-property-decorator'
export default class FaceLogo extends Vue {
  @Prop(String) readonly myName: string | undefined
  age = 21
}
</script>

<style>
.my-face {
  width: 200px;
}
</style>
