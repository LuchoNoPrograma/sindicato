<template>
  <form>
    <label for="nombre">Nombre:</label>
    <input type="text" name="persona.nombre" id="nombre">
    <input type="text" name="persona.ci" id="nombre">
    <ButtonPrimary :text-button="'Hola papus'"></ButtonPrimary>
  </form>
</template>

<script>
import ButtonPrimary from "@/components/ui-elements/ButtonPrimary.vue";

export default {
  data() {
    return {
      persona: {
        nombre: '',
        paterno: '',
        materno: '',
        ci: '',
        email: '',
        telefono: '',
      }
    }
  },
  methods: {
    async enviarFormulario() {
      await fetch('/api/persona', {
        headers: {'Content-Type': 'application/json'},
        body: JSON.stringify(this.persona)
      })
    }
  },
  components:{
    ButtonPrimary
  }
}
</script>

<style>
</style>