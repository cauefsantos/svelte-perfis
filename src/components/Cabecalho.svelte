<script lang="ts">
  import Formulario from '../components/Formulario.svelte';
  import Titulo from '../components/Titulo.svelte';
</script>

<header>
  <Titulo />
  
  <div class="busca-usuario">
    <Formulario on:aoAlterarUsuario />
  </div>
</header>

<style>
  header {    
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .busca-usuario {
    position: relative;
    width: 70%;
  }
</style>