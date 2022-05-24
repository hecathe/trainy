<template>
  <ul class="event-list">
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
  .event-list {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    column-gap: 20px;
  }
</style>>