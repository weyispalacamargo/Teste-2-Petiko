<script setup>
import FilePreview from "./filePreview.vue";
import axios from "axios";
</script>
<script>
export default {
  name: 'FormItem',
  data() {
    return {
      dataForm:{}
    };
  },
  methods: {
    register(){
      axios.post(`${process.env.VUE_APP_URL}register`,this.dataForm).then((response)=>{
        console.log(response.data)
      }).catch((error)=>{
        console.log(error)
      })
    }
  },
};
</script>
<template>
  <div>
    <p>Preencha o formulário antes de fazer o pedido:</p>
    <form>
      <div class="inputContainer">
        <label for="CPF">CPF:</label>
        <input
          type="text"
          id="cpf"
          name="cpf"
          v-model="dataForm.cpf"
          placeholder="Digite o seu CPF"
        />
      </div>
      <div class="inputContainer">
        <label for="Telefone">Telefone:</label>
        <input
          type="text"
          id="telefone"
          name="telefone"
          v-model="dataForm.telefone"
          placeholder="Digite o seu Telefone"
        />
      </div>
      <div class="inputContainer">
        <label for="Email">Email:</label>
        <input
          type="email"
          id="email"
          name="email"
          v-model="dataForm.email"
          placeholder="Digite o seu Email"
        />
      </div>
      <div class="inputContainer">
        <FilePreview />
      </div>
      <div class="inputContainer">
        <button type="button" @click="register()">Registrar</button>
      </div>
    </form>
  </div>
</template>

<style scoped>
</style>