<template>
  <div class="app">
    <h1>My App</h1>
    <Notification :message="notificationMessage" @close="closeNotification" v-if="showNotification" />
    <button @click="showNotification = !showNotification">Toggle Notification</button>
  </div>
</template>

<script>
import Notification from './components/NotificationDemo.vue';

export default {
  components: {
    Notification,
  },
  data() {
    return {
      showNotification: false,
      notificationMessage: 'Hello, World!',
    };
  },
  methods: {
    closeNotification() {
      this.showNotification = false;
    },
  },
};
</script>

<style>
.app {
  padding: 20px;
}

button {
  background-color: #e0e0e0;
  border: none;
  padding: 10px 20px;
}
</style>