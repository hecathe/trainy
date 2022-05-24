<template>
  <li class="tag-item">{{ tag.name }}</li>
</template>

<script>
export default {
  props: {
    tag: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
  .tag-item {
    display: flex;
    font-weight: 700;
    font-size: 14px;
    line-height: 20px;
    color: #68717B;
    background: #EBEDEE;
    border-radius: 2px;
    padding: 0 4px;
  }
</style>