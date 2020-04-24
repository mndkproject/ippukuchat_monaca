<template>
  <v-ons-page>
    <v-ons-list>
      <v-ons-list-item tappable @click="toContent">mendako</v-ons-list-item>
    </v-ons-list>
  </v-ons-page>
</template>

<script>
  export default {
    methods: {
      toContent() {
        this.$emit('to-content');
      }
    }
  }
</script>
