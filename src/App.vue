<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld/>
    <SimpleForm/>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'
import SimpleForm from "@/components/SimpleForm.vue";

export default {
  name: 'App',
  components: {
    HelloWorld,
    SimpleForm
  }
}
</script>

<style src="./assets/tailwind.css">
</style>
