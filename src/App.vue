<template>
  <div>
    <div>
      One-way data binding<br>
      Two-way data binding<br>
      v-model -> formulários
    </div>
    <br><br>
    <div>
      <label>Nome</label><br>
      <input
        v-model="name"
        type="text"
        > <br>
        {{ name }}
    </div>
    <br><br>
    <div>
      <label>Sports</label><br>
      <select v-model="sports">
        <option value="">Escolha</option>
        <option value="futebol">Futebol</option>
        <option value="skate">skate</option>
        <option value="tenis">tenis</option>
      </select><br>
      {{ sports }}
    </div>
    <br><br>
    <div>
      <label> Newsletter</label><br>
      <input
        v-model="newsletter"
        type="radio"
        value="Sim"
      > Sim

      <input
        v-model="newsletter"
        type="radio"
        value="Não"
      > Não <br>
      {{ newsletter }}

    </div>
    <br><br>
    <div>
      <label> Contrato</label><br>
      <input
        v-model="contract"
        type="checkbox"
        value="Sim"
      > Aceita os termos <br>

      {{ contract }}

    </div>
    <div>
      <label> Colors </label><br>
      <input
        v-model="colors"
        type="checkbox"
        value="Blue"
      > Blue

      <input
        v-model="colors"
        type="checkbox"
        value="Red"
      > Red <br>
      {{ colors }}

    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      name:'Jon Snow',
      sports:'',
      newsletter:'',
      contract: false,
      colors:[]
    }

  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
