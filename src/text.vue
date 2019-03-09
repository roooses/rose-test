<template>
  <div :style="data.style.container" v-html="text"></div>
</template>

<script>
export default {
  name: 'RText',
  props: {
    data: {
      type: Object,
      default: ''
    }
  },
  data() {
    return {
      text: ''
    }
  },
  watch: {
    'data.text' () {
      this.text = unescape(this.data.text)
    }
  },
  created () {
    this.text = unescape(this.data.text)
  }
}
</script>
<style lang="scss">
  .ql-align-center {
    text-align: center;
  }

  .ql-align-right {
    text-align: right;
  }
</style>


