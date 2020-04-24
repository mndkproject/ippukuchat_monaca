<template>
  <v-ons-page>
    <div class="content">
      <v-ons-button modifier="large" @click="push">Login</v-ons-button>
    </div>
  </v-ons-page>
</template>

<script>
  import tabber from './tabber';

  export default {
     methods: {
       pop(){
         this.pageStack.pop();
       },
       push() {
         this.pageStack.push(tabber);
       }
     },
     props: ['pageStack'],
     key: 'key_login',
  }
</script>