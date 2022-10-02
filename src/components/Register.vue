<script setup>
import NameInput from './Inputs/NameInput.vue';
import MailInput from './Inputs/MailInput.vue';
import PhoneInput from './Inputs/PhoneInput.vue';
import PasswordInput from './Inputs/PasswordInput.vue';
import { ref } from 'vue';

const registerData = ref({
	fullname: {
		value: "",
		isValid: true
	},
	email: {
		value: "",
		isValid: true
	},
	phone: {
		value: "",
		isValid: true
	},
	password: {
		value: "",
		isValid: true
	},
	rePassword: {
		value: "",
		isValid: true
	},
})
</script>

<template>
	<div class="wrapper">
		<h1>Register</h1>
		<div>
			<NameInput v-model:name="registerData.fullname.value" v-model:validation="registerData.fullname.isValid" />
			<MailInput />
			<PhoneInput />
			<PasswordInput />
			<PasswordInput />
		</div>
		<div>
			<button>Register</button>
			<button>Have an account</button>
		</div>
	</div>
</template>

<style scoped>

</style>