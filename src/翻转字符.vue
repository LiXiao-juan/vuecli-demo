<template>
  <div>
    <h1>{{ msg }}</h1>
    <button @click="btn">点我翻转</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg:"Hello,vue"
    }
  },
  methods:{
    btn(){
      this.msg=this.msg.split('').reverse().join('')
    }
  }
}
</script>

<style>

</style>