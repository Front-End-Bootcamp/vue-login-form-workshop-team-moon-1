
<script setup>
	import { ref, computed } from 'vue'
	const props = defineProps(["phone"])
	const emits = defineEmits(["update:phone", "update:phoneNumberValid"])
	const phoneNumberPattern = /^[\+]?[(]?[0-9]{3}[)]?[-\s\.]?[0-9]{3}[-\s\.]?[0-9]{4,6}$/im
	const phoneNumberValid = computed(() => phoneNumberPattern.test(props.phone))
	const phoneHandler = (event) => {
		phone.value = event.target.value
		phoneNumberValid.value = phone.value.length > 0
		emits("update:phone", phone.value)
		emits("update:phoneNumberValid", phoneNumberValid.value)
	}

</script>

<template>
	
	<input type="text" :value="props.phone" @input="phoneHandler" :class="phoneClass" />

</template>