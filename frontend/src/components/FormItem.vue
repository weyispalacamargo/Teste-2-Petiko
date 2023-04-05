<script setup>
import FilePreview from "./filePreview.vue";
import axios from "axios";
</script>
<script>
export default {
  data() {
    return {
      cpf: "",
      telefone: "",
      email: "",
    };
  },
  methods: {
    palletsForm() {
      axios
        .post("//jsonplaceholder.typicode.com/posts", {
          cpf: this.cpf,
          telefone: this.telefone,
          email: this.email,
        })
        .then((response) => {
          //console.log(response);
          //this.response = response.data;
          this.success = "Data saved successfully";
          this.response = JSON.stringify(response, null, 2);
        })
        .catch((error) => {
          this.response = "Error: " + error.response.status;
        });
      this.cpf = "";
      this.telefone = "";
      this.email = "";
    },
  },
};
</script>
<template>
  <div>
    <p>Preencha o formulário antes de fazer o pedido:</p>
    <form @submit.prevent="palletsForm">
      <div class="inputContainer">
        <label for="CPF">CPF:</label>
        <input
          type="text"
          id="cpf"
          name="cpf"
          v-model="cpf"
          placeholder="Digite o seu CPF"
        />
      </div>
      <div class="inputContainer">
        <label for="Telefone">Telefone:</label>
        <input
          type="text"
          id="telefone"
          name="telefone"
          v-model="telefone"
          placeholder="Digite o seu Telefone"
        />
      </div>
      <div class="inputContainer">
        <label for="Email">Email:</label>
        <input
          type="email"
          id="email"
          name="email"
          v-model="email"
          placeholder="Digite o seu Email"
        />
      </div>
      <div class="inputContainer">
        <FilePreview />
      </div>
      <div class="inputContainer">
        <button type="submit">Enviar</button>
      </div>
      <h3>Data retrieved from server:</h3>
      <p v-if="success">{{ success }}</p>
      <pre>{{ response }}</pre>
    </form>
  </div>
</template>

<style scoped>
</style>