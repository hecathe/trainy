<template>
  <button class="btn">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'default-button'
}
</script>

<style scoped>
  .btn {
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    color: #ffffff;
    background: #f4691b;
    border: none;
    border-radius: 4px;
    padding: 4px 12px;
    cursor: pointer;
  }
</style>