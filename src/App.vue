<template>
  <div>
    <my-addtion></my-addtion>
    <p>---------------------------------------------</p>
    <my-sub></my-sub>
  </div>
</template>

<script>
import Addtion from './components/Addition.vue'
import Sub from './components/Sub.vue'
export default {
  data () {
    return {}
  },
  components: {
    'my-addtion': Addtion,
    'my-sub': Sub
  }
}
</script>

<style></style>
