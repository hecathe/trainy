<template>
  <li class="list-item">
    <h3 class="list-item__title">{{ event.name }}</h3>
    <div class="list-item__bot">
      <tag-list :tags="tags"></tag-list>
      <default-button>Подробнее</default-button>
    </div>
  </li>
</template>

<script>
import DefaultButton from '@/components/UI/DefaultButton.vue';
import TagList from '@/components/TagList.vue';
// import axios from 'axios'

export default {
  components: {
    DefaultButton,
    TagList
  },
  props: {
    event: {
      type: Object,
      required: true,
    }
  },
  data() {
    return {
      // tags: this.event,
      // tags: this.event.title
      tags: []
    }
  },
  methods: {
    // async fetchTags() {
    //   const response = await axios.get('')
    // }
    objectToArr() {
      // console.log(this.event.company);
      for (const key in this.event.company) {
        if (this.event.company.hasOwnProperty(key)) {
          this.tags.push(key)
          console.log(this.tags);
        }
      }
    }
  },
  mounted() {
    this.objectToArr()
  }
}
</script>

<style scoped>
  .list-item {
    background-color: #F4F5F6;
    border: 1px solid #FFFFFF;
    border-radius: 4px;
    padding: 20px;
  }

  .list-item__title {
    font-weight: 700;
    font-size: 16px;
    line-height: 20px;
    margin: 0;
    margin-bottom: 20px;
  }

  .list-item__bot {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
  }
</style>