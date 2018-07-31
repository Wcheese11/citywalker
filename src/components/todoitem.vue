<template>
<li class="item" @click="handDelete">{{content}}</li>
</template>

<script>
export default {
  props: ['content', 'index'],
  methods: {
    handDelete () {
      this.$emit('delete', this.index)
    }
  }
}
</script>

<style scoped>
  .item{
    color: blue;
  }
</style>
