<template>
  <li class="event-item">
    <h3>title</h3>
    <div>
      <div class="tags">
        <div class="tag">tag</div>
      </div>
      <button>Подробнее</button>
    </div>
  </li>
</template>

<script>
export default {
  props: {
    event: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style scoped>
  .event-item {
    background-color: #F4F5F6;
    border: 1px solid #FFFFFF;
    border-radius: 4px;
  }
</style>