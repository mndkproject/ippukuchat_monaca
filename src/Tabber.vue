<template>
  <v-ons-page>
    <v-ons-tabbar swipeable position="top" :tabs="tabs" :visible="true" :index.sync="activeIndex" @to-content="toContent" @to-logout="toLogout"></v-ons-tabbar>
  </v-ons-page>
</template>

<script>
  import customToolbar from './CustomToolbar';
  import content from './Content';

  import settingsPage from './tabitem/Settings';
  import memberPage from './tabitem/Member';
  import chatPage from './tabitem/Chat';

  export default {
    data() {
      return {
        activeIndex: 0,
        tabs: [
	  {
	    icon: this.md() ? 'ion-android-people' : 'ion-ios-people',
	    label: 'Member',
	    page: memberPage
	  },
	  {
	    icon: this.md() ? 'ion-android-chat' : 'ion-ios-chatboxes',
	    label: 'Chat',
	    page: chatPage,
	    badge: ''
	  },
	  {
	    icon: this.md() ? 'ion-android-settings' : 'ion-ios-settings',
	    label: 'Settings',
	    page: settingsPage
	  }
        ]
      };
    },
    methods: {
      pop() {
        this.pageStack.pop();
      },
      push() {
        this.pageStack.push(content);
      },
      md() {
        return this.$ons.platform.isAndroid();
      },
      toContent() {
        this.pageStack.push(content);
      },
      toLogout() {
        this.pageStack.pop();
      }
    },
    computed: {
      title() {
        return this.tabs[this.activeIndex].label;
      }
    },
    props: ['pageStack'],
    components: { customToolbar, memberPage, settingsPage, chatPage },
    key: 'key_tabber'
  }
</script>
