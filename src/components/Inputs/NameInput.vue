<script setup>
import { computed } from 'vue';

	const props = defineProps(["name", "validation"])
	const emits = defineEmits(["update:name","update:validation"])
	const pattern = /^([a-zA-ZğüşöçİĞÜŞÖÇ'-.]+ [a-zA-ZğüşöçİĞÜŞÖÇ'-.]+)$/
	const isValid = computed(() => pattern.test(props.name))
	const nameHandler = (event) => {
		emits("update:name",event.target.value)
		emits("update:validation", isValid.value)
	}
</script>

<template>
	<input type="text" :value="props.name" @input="nameHandler" /> 
</template>