<template>
  <div class="screen">
    <h1>Chúc mừng</h1>
    <p>{{ Math.round(timer / 1000) }}seconds</p>
    <button @click="onStartAgain">Bắt đầu lại</button>
  </div>
</template>

<script>
export default {
  props: {
    timer: {
      type: Number,
      required: true,
    },
  },
  methods: {
    onStartAgain() {
      this.$emit("onStartAgain"); //gửi sự kiên lên Ápp
    },
  },
};
</script>
