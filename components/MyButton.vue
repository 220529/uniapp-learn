<template>
  <button class="my-btn" @click="handleClick">
    <slot>{{ text }}</slot>
  </button>
</template>

<script>
export default {
  name: 'MyButton',
  props: {
    text: {
      type: String,
      default: '按钮'
    }
  },
  methods: {
    handleClick() {
      this.$emit('click');
    }
  }
}
</script>

<style scoped>
.my-btn {
  padding: 10px 24px;
  background: #4B7BEC;
  color: #fff;
  border: none;
  border-radius: 6px;
  font-size: 16px;
}
</style> 