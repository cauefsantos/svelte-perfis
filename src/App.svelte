<script lang="ts">
  import Cabecalho from './components/Cabecalho.svelte';
  import Usuario from './components/Usuario.svelte';
	import type IUsuario from './interfaces/IUsuario';

	let usuario: IUsuario | null = null;

  function definirUsuario(evento: CustomEvent<IUsuario>) {
    usuario = evento.detail;
  }

</script>


<div class="app">
	<header>
		<Cabecalho on:aoAlterarUsuario={definirUsuario} />
	</header>

  {#if usuario}
    <Usuario {usuario} />
  {/if}
</div>

<style>
	.app {
    max-height: 100vh;
  }

  header {    
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
</style>
