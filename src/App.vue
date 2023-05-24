<template>
  <div class="card">
      Teste
    <BaseCard />
  </div>
</template>


<script>
import BaseCard from '@/components/BaseCard.vue';

export default {
    name: "App",
    components: { BaseCard },
    data() {
      return {        
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
    },
    updated() {
    },
    beforeCreate() {
    },
    created() {
    },
    beforeMount() {
    },
    mounted() {
    },
    beforeUnmount() {
    },
    unmounted() {
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
