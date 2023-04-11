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

const Cadastrar = ref(false)

function Confirmar() {
  if (senha.value != confirmarSenha.value) {
    alert('semha incorreta!')
  } else {
    Cadastrar.value = !Cadastrar.value
  }
}
</script>

<template>
  <div class="container">
    <div class="login">

      <h2>login</h2>

      <label>Nome:</label>
      <input
        type="text"
        v-model.trim="nome"
        placeholder="Digite seu nome"
        maxlength="30"
        minlength="3"
      />

      <label>E-mail:</label>
      <input type="email" v-model="email" placeholder="Digite seu e-mail" />

      <label>Senha:</label>
      <input type="password" v-model="senha" placeholder="digite sua senha" maxlength="20" minlength="4" />
      <label>Confirmar senha:</label>
      <input type="password" v-model="confirmarSenha" placeholder="confirme sua senha" />

      <label>Data de nascimento:</label>
      <input type="date" v-model="nascimento" />

      <label>Endereço:</label>
      <input type="text" v-model="endereco" placeholder="digite o seu endereço" maxlength="30" />

      <label>Cidade:</label>
      <input type="text" v-model="cidade" maxlength="25"/>

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
      <input type="text" v-model="hobbies" placeholder="digite alguns hobbies seus" maxlength="30" minlength="5" />

      <label>Linguagem de programação</label>
      <input
        type="text"
        v-model="lingProg"
        placeholder="Digite a linguagem de programação que você mais usa"
        size="50"
      />

      <label>Biografia:</label>
      <input
        type="text"
        v-model="bio"
        maxlength="200"
        minlength="4"
        placeholder="Adicione sua biografia"
      />
      <p></p>
      <button @click="Confirmar" class="btn btn-primary">Cadastrar</button>
    </div>
    <div class="info" v-if="Cadastrar">
      <h2>suas informações</h2>
      <p>Nome: {{ nome }}</p>
      <p>Email: {{ email }}</p>
      <p>Senha: {{ senha }}</p>
      <p>Data de nascimento: {{ nascimento }}</p>
      <p>Estado: {{ estado }}</p>
      <p>Hobbie: {{ hobbies }}</p>
      <p>Linguagem de programação: {{ lingProg }}</p>
      <p class="text-bio">Biografia: {{ bio }}</p>
    </div>
  </div>
</template>

<style scoped>
button {
  background-color: rgb(151, 192, 247);
  color: white;
  border-radius: 10px;
  width: 100px;
  
}

.container {
  background-color: rgb(248, 247, 247);
  border-radius: 5px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  justify-content: center;
  color: white;
  background-color: rgb(0, 0, 0);
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
  width: 500px;
}

.info {
  width: 500px;
}

h2 {
text-align: center;

}
</style>
