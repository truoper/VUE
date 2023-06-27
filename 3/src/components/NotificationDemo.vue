<template>
  <div class="notification">
    <div class="content">
      <p>{{ message }}</p>
      <button @click="closeNotification">Close</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    message: {
      type: String,
      required: true,
    },
  },
  methods: {
    closeNotification() {
      this.$emit('close');
    },
  },
};
</script>

<style scoped>
.NotificationDemo {
  background-color: #f0f0f0;
  padding: 10px;
  margin-bottom: 10px;
}

.content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

button {
  background-color: #e0e0e0;
  border: none;
  padding: 5px 10px;
}
</style>