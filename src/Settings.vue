<template>
  <v-ons-page>
    <p style="text-align: center">
      Change the settings.
      <v-ons-button modifier="large" @click="toLogout">ログアウト</v-ons-button>
    </p>
  </v-ons-page>
</template>

<script>
  export default {
    methods: {
      toLogout() {
        this.$emit('to-logout');
      }
    }
  }
</script>