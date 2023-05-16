<template>
  <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
    {{textButton}}
  </button>
</template>

<script>
export default {
  name: 'ButtonPrimary',
  props: {
    textButton: String
  }
}
</script>

<style>
</style>