<template>
  <div>singer页面</div>
</template>

<script>
import {getSingerList} from '@/api/singer'

export default {
  data () {
    return {}
  },
  created () {
    this._getSingerList()
  },
  methods: {
    _getSingerList () {
      getSingerList().then((res) => {
        if (res.code === 0) {
          console.log(res.data.list)
        }
      })
    }
  }
}
</script>

<style lang="stylus" scoped>

</style>
