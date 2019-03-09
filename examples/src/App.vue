<template>
  <div id="app">
    <RText :data="data"></RText>
  </div>
</template>

<script>
import data from '../../config/index.json'

export default {
  name: 'App',
  data () {
    return {
      data: data.data
    }
  }
}
</script>
