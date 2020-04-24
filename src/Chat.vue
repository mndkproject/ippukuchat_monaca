<template>
  <v-ons-page>
    <p style="text-align: center">
      Some news here.
      <v-ons-button modifier="large" @click="toHome">go to home</v-ons-button>
      <v-ons-button modifier="large" @click="toContent">go to content</v-ons-button>
    </p>
  </v-ons-page>
</template>

<script>
  export default {
    methods: {
      toHome() {
        this.$emit('change-tab', 0);
      },
      toContent() {
        this.$emit('to-content');
      }
    }
  }
</script>
