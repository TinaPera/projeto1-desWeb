<script setup>
import { ref } from 'vue'

const nome = ref('')
const email = ref('')
const senha = ref('')
const confirmarSenha = ref('')
const nascimento = ref('')
const endereco = ref('')
const cidade = ref('')
const estado = ref('')
const hobbies = ref('')
const lingProg = ref('')
const bio = ref('')

const cadastro = ref(true)
</script>

<template>
<div class="container">
    <div class="login">
  <label>Nome:</label>
  <input type="text" v-model.trim="nome" placeholder="Digite seu nome" maxlength="30" minlength="3">
  
  <label>E-mail:</label>
  <input type="email" v-model="email" placeholder="Digite seu e-mail">
  
  <label>Senha:</label>
  <input type="password" v-model="senha" placeholder="digite sua senha">
  <label>Confirmar senha:</label>
  <input type="password" v-model="confirmarSenha" placeholder="confirme sua senha">
  
  <label>Data de nascimento:</label>
  <input type="date" v-model="nascimento">
  
  <label>Endereço:</label>
  <input type="text" v-model="endereco" placeholder="digite o seu endereço">
  
  <label>Cidade:</label>
  <input type="text" v-model="cidade">
  
  <label>Estado:</label>
  <select v-model="estado">
    <option value="AC">Acre</option>
    <option value="AL">Alagoas</option>
    <option value="AP">Amapá</option>
    <option value="AM">Amazonas</option>
    <option value="BA">Bahia</option>
    <option value="CE">Ceará</option>
    <option value="DF">Distrito Federal</option>
    <option value="ES">Espírito Santo</option>
    <option value="GO">Goiania</option>
    <option value="MA">Maranhão</option>
    <option value="MT">Mato Grosso</option>
    <option value="MS">Mato Grosso do Sul</option>
    <option value="MG">Minas Gerais</option>
    <option value="PA">Pará</option>
    <option value="PB">Paraíba</option>
    <option value="PR">Paraná</option>
    <option value="PE">Pernambuco</option>
    <option value="PI">Piauí</option>
    <option value="RJ">Rio de Janeiro</option>
    <option value="RN">Rio Grande do Norte</option>
    <option value="RS">Rio Grande do Sul</option>
    <option value="RO">Rondonia</option>
    <option value="RR">Roraima</option>
    <option value="SC">Santa Catarina</option>
    <option value="SP">São Paulo</option>
    <option value="SE">Sergipe</option>
    <option value="TO">Tocantins</option>
  </select>

  <label>hobbies:</label>
  <input type="text" v-model="hobbies" placeholder="digite alguns hobbies seus">
  
  <label>Linguagem de programação</label>
  <input type="text" v-model="lingProg" placeholder="Digite a linguagem de programação que você mais usa" size="50">
  
  <label>Biografia:</label>
  <input type="text" v-model="bio" maxlength="200" minlength="4" placeholder="Adicione sua biografia">
</div>
  <div>
  <button @click="cadastro">Cadastrar</button>
  </div>
</div>
</template>

<style scoped>
  button {
    background-color: rgb(151, 192, 247);
    color: white;
    border-radius: 10px;
  }

  .container {
    background-color: rgb(248, 247, 247);
    border-radius: 5px;
  }

  input {
    border-radius: 10px;
    
  }

  select {
    border-radius: 10px;
  }

  .login {
    display: grid;
    grid-template-rows: 1fr;
  }
  
</style>
