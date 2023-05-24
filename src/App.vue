<template>
  <div>
    <COMPONENTE>
      
    </COMPONENTE>
    <BaseAlert
      v-if="showAlert"
      :variant="variant"
      @close="onClose()"
      >
      {{ text }}
      </BaseAlert>
        
  </div>
</template>


<script>
import BaseAlert from '@/components/BaseAlert.vue';
export default {
    name: "App",
    components: { BaseAlert },
    data() {
      return {  
        showAlert: true,
        variant: 'success',      
        text: 'Seu formulário foi enviado com sucesso!'      
        }
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
      onClose(){
        this.showAlert=false
          console.log('on close');
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
