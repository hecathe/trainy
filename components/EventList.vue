<template>
  <ul class="list">
    <event-item v-for="event in events" :event="event" :key="event.id"></event-item>
  </ul>
</template>

<script>
import EventItem from '@/components/EventItem.vue';

export default {
  components: {
    EventItem
  },
  props: {
    events: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
  .list {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    column-gap: 20px;
    row-gap: 20px;
    list-style: none;
    padding: 0;
    margin: 0;
  }
</style>>