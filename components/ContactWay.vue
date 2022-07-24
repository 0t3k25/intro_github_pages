<template>
  <v-container pt-5>
    <v-row>
      <v-col cols="12" align="center" class="text-h4">連絡方法</v-col>
    </v-row>

    <v-row>
      <v-col cols="6" align="center"
        ><v-text-field
          v-model="email"
          filled
          color="deep-purple"
          label="name"
          type="name"
        ></v-text-field
      ></v-col>
      <v-col cols="6" align="center"
        ><v-text-field
          v-model="email"
          filled
          color="deep-purple"
          label="Email address"
          type="email"
        ></v-text-field
      ></v-col>
    </v-row>
    <v-row>
      <v-col cols="12" align="center"
        ><v-text-field
          v-model="email"
          filled
          color="deep-purple"
          label="comment"
          type="comment"
        ></v-text-field
      ></v-col>
    </v-row>
    <v-row>
      <v-checkbox v-model="agreement" color="deep-purple">
        <template v-slot:label>
          I agree to the&nbsp;
          <a href="#" @click.stop.prevent="dialog = true">Terms of Service</a>
          &nbsp;and&nbsp;
          <a href="#" @click.stop.prevent="dialog = true">Privacy Policy</a>*
        </template>
      </v-checkbox>
    </v-row>

    <v-divider></v-divider>
    <v-row class="pt-6">
      <v-btn
        :disabled="!form"
        :loading="isLoading"
        class="white--text"
        color="deep-purple accent-4"
        depressed
      >
        Submit
      </v-btn>
    </v-row>
  </v-container>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'

@Component
export default class TimeLine extends Vue {
  email: undefined
}
</script>
