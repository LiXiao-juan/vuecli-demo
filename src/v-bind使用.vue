<template>
  <div>
    <a :href="url">点我去百度</a>
  </div>
</template>

<script>
export default {
  data() {
    return {
      url: 'http://www.baidu.com'
    }
  },
}
</script>

<style>

</style>