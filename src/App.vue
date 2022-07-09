<template>
	<div class="container">
		<h1 class="text-center">API Paises</h1>
		<Continentes />
		<Buscador />
		<CardList />
	</div>
</template>

<script>
import Buscador from './components/Buscador.vue'

import CardList from './components/CardList.vue'
import Continentes from './components/Continentes.vue'

export default {
	name: 'App',
	components: {
		CardList,
		Continentes,
		Buscador,

	}
}
</script>