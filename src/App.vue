<template>
  <v-ons-navigator :page-stack="pageStack">
    <component :is="page" v-for="page in pageStack" :key="page.key" :page-stack="pageStack"></component>
  </v-ons-navigator>
</template>

<script>
  import login from './login';
  import tabber from './tabber';
  import content from './content';

  export default {
    data() {
      return {
        pageStack: [login]
      }
    }
  }
</script>
