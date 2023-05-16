<template>
  <div class="text-emerald-950">
    {{msg}}
  </div>
</template>
<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: ''
    }
  },
  mounted() {
    fetch('/api/mensaje/saludo')
        .then((response) => response.text())
        .then((data) => {
          this.msg = data;
        })
  }

}
</script>

<style scoped>
</style>
