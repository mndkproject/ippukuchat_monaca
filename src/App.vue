<template>
  <v-ons-navigator :page-stack="pageStack">
    <component :is="page" v-for="page in pageStack" :key="page.key" :page-stack="pageStack"></component>
  </v-ons-navigator>
</template>

<script>
  import login from './Login';
  import tabber from './Tabber';
  import content from './Content';

  export default {
    data() {
      return {
        pageStack: [login]
      }
    }
  }
</script>
