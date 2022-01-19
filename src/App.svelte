<script>
	import Converter from "./Converter.svelte";
	import Sobre from "./Sobre.svelte";
	import Menu from "./Menu.svelte";

	import {estado} from "./Estado"
</script>

{#if $estado === 'menu'}
	<!-- notem como cada componente/módulo que crianos no svelte vira um tag -->
	<Menu/>
{:else if $estado === 'sobre'}
	<Sobre/>
{:else if $estado === 'converter'}
	<Converter/>
{/if}
