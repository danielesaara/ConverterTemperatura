<script>
	import { estado } from './Estado.js'
	import { trocarEstadoDoJogo } from './Estado.js'
</script>

<h1>
	Converter Temperatura
</h1>

<div class='menu' on:click={() => trocarEstadoDoJogo('sobre')}>
	Sobre
</div>

<div class='menu' on:click={() => trocarEstadoDoJogo('converter')}>
	Converter Temperatura
</div>