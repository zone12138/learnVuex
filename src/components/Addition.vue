<template>
  <div>
    <p>当前值为：{{ $store.state.counter }}</p>
    <button @click="funHandle">+1</button>

    <button @click="funHandle1">+2</button>
  </div>
</template>

<script>
import { mapState, mapMutations } from 'vuex'
export default {
  data () {
    return {}
  },
  computed: {
    ...mapState(['counter'])
  },
  methods: {
    // 两种方式调用 store 中的 mutation 函数
    // 1. import 引入 mapMutations , 调用他去映射到methods中去 , 函数可以通过调用映射的名称去调用mutation里面的函数
    ...mapMutations(['add', 'addN']),
    funHandle () {
      this.add()
      window.console.log({ ...mapState(['counter']) })
    },

    // 2.不用去引入 mapMutations , 直接使用 this.$store.commit(name, argument) name为mutation里面的函数名称, argument为传参
    funHandle1 () {
      this.$store.commit('addN', 2)
    }
  }
}
</script>

<style></style>
