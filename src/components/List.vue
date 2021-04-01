<template>
  <div class="list">
    <div class="listheader">
      <p class="list-title">{{ title }}</p>
      <div class="deletelist" @click="removeList">×</div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      title: {
        type: String,
        required: true
      },
      listIndex: {
        type: Number,
        required: true
      }
    },
    methods: {
      removeList: function () {
        this.$store.dispatch('removelist', { listIndex: this.listIndex})
      }
    }
  }
</script>
