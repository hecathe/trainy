<template>
  <ul class="tag-list">
    <tag-item v-for="tag in tags" :tag="tag" :key="tag.id"></tag-item>
  </ul>
</template>

<script>
import TagItem from '@/components/TagItem.vue';

export default {
  components: {
    TagItem
  },
  props: {
    tags: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
  .tag-list {
    display: flex;
    flex-wrap: wrap;
    column-gap: 10px;
    list-style: none;
    padding: 0;
    margin: 0;
  }
</style>