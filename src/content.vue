<template>
  <v-ons-page>
    <custom-toolbar :back-label="'戻る'">content</custom-toolbar>
    <div class="content">
      content
    </div>
  </v-ons-page>
</template>

<script>
  import customToolbar from './CustomToolbar';

  export default {
    methods: {
      pop() {
        this.pageStack.pop();
      }
    },
    props: ['pageStack'],
    components: { customToolbar },
    key: 'key_content',
  }
</script>
