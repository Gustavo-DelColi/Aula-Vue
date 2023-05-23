<template>
  <div>
    <TheHeader v-if="showHeader"/>
    <h1>Hello World</h1>
    {{ name }} <br>
    <button @click="showHeader = !showHeader">
      Ativar e desativar
    </button>
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';

export default {
    name: "App",
    components: { TheHeader },
    data() {
      return {
        name: "Han Solo",
        showHeader: true,
        };
    },
    // Criacao
    // Preparar o componente
    // Ajax, inicializar algumas variáveis
    // Não tem acesso ao template (DOM)
    // Montagem
    // Inicializar um lib externa
    // Precisa de acesso ao template (DOM)
    // Tem acesso ao template (DOM)
    // Atualizacao
    // Debug
    // Update
    // Desmontagem
    // Remover tudo que for necessario (lib->destroy()) para Liberar memória
    // HOOKS 
    beforeUpdate() {
        console.log("beforeUpdate", this.name);
    },
    updated() {
        console.log("updated", this.name);
    },
    beforeCreate() {
        console.log("beforeCreate");
        console.log("Estado:", this.name);
        console.log("DOM:", this.$el);
    },
    created() {
        console.log("created");
        console.log("Estado:", this.name);
        console.log("DOM:", this.$el);
    },
    beforeMount() {
        console.log("beforeMount");
        console.log("Estado:", this.name);
        console.log("DOM:", this.$el);
    },
    mounted() {
        console.log("mounted");
        console.log("Estado:", this.name);
        console.log("DOM:", this.$el);
    },
    beforeUnmount() {
        console.log("beforeUnmount");
        console.log("Estado:", this.name);
        console.log("DOM:", this.$el);
    },
    unmounted() {
        console.log("unmounted");
        console.log("Estado:", this.name);
        console.log("DOM:", this.$el);
    },
    watch: {},
    computed: {},
    methods: {
      toggleHeader(){
        this.showHeader = !this.showHeader
      }
    },
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
