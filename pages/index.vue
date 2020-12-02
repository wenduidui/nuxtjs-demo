<template>
  <div>
    <h1>{{title}}</h1>
    <nuxt-link to="/about">abou发发发t</nuxt-link>
    <br>
    <foo :posts="posts" />
  </div>
</template>

<script>
import axios from 'axios'
import Foo from '@/components/Foo'
export default {
  name: 'HomePage',
  components: {
    Foo
  },
  // 当你想要动态页面内容有利于SEO 或者是提升首屏渲染速度的时候,就在asyncData中发请求拿数据
  async asyncData() {
    const res = await axios({
      method: 'GET',
      url: 'http://localhost:3000/data.json'
    })
    return res.data
  },
  // 如果是非异数据或者普通数据,则正常的初始化到 data 中即可
  data () {
    return {
    }
  },
  methods: {}
}
</script>

<style lang='less'>

</style>
