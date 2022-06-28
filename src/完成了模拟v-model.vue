<template>
  <div>
    <input type="text" @input="inputFn" :value="val" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      val: '',
    }
  },
  methods: {
    inputFn(e) {
      this.val = e.target.value
    },
  },
}
</script>

<style></style>
