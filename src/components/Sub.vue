<template>
  <div>
    <p>当前值为：{{counter}}</p>
    <button>-</button>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  data () {
    return {}
  },
  computed: {
    ...mapState(['counter'])
  }
}
</script>

<style></style>
