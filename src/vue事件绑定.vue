<template>
  <div>
    <!-- vue指令:   v-on事件绑定-->
    <p>你要买商品的数量: {{ count }}</p>
    <button v-on:click="count = count + 1">增加1</button>
    <button v-on:click="addFn">增加1个</button>
    <button v-on:click="addCountFn(5)">一次加5件</button>

    <button @click="subFn">减少</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
    count:0  
    }
  },
  methods: {
    addFn() {
      // this代表export default后面的组件对象(下属有data里return出来的属性)
      this.count++
    },
    addCountFn(num) {
      this.count += num
    },
    subFn() {
      this.count--
    },
  },
}
</script>

<style></style>
