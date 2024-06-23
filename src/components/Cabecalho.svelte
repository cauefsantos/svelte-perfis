<script lang="ts">
  import Formulario from '../components/Formulario.svelte';
  import Titulo from '../components/Titulo.svelte';
</script>

<Titulo />

<div class="busca-usuario">
  <Formulario on:aoAlterarUsuario />
</div>

<style>
  .busca-usuario {
    position: relative;
    width: 70%;
  }
</style>