<template>
  <div>
    <h1>FooPage</h1>
    <ul>
        <li v-for="item in posts" :key="item.id">{{item.title}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'FooPage',
  props: ['posts'],
  methods: {}
}
</script>

<style lang='less'>

</style>
