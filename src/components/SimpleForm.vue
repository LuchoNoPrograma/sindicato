<template>
  <form>
    <label for="nombre">Nombre:</label>
    <input type="text" name="persona.nombre" id="nombre">
    <input type="text" name="persona.ci" id="nombre">
    <button type="submit">Registrar</button>
  </form>
</template>

<script>
export default{
  data(){
   return{
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
  async created(){
    this.persona = fetch('/api/persona',{
      method: 'POST',
      headers: {'Content-Type': 'application/json'},
    })
  },
  methods: {
    async enviarFormulario(){
      const response = await fetch('/api/persona', {
        headers: {'Content-Type': 'application/json'},
        body: JSON.stringify(this.persona)
      })
    }
  }
}
</script>

<style scoped>
button{
  padding: 2em;
  background-color: #006666;
  border-radius: 1em;
}
</style>