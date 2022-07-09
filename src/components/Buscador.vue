<template>
	<input 
		type="text" 
		class="form-control my-3"
		placeholder="Ingrese un País"
		v-model="texto"
		@keyup="buscarInput">
</template>

<script>
import { ref } from '@vue/reactivity'
import {useStore} from 'vuex'
export default {
	setup(){
		
		const store = useStore()
		const texto = ref('')


		const buscarInput = () => {
			return store.dispatch('filtrarNombre',texto.value)
		}

		return {texto, buscarInput}
	}
}
</script>