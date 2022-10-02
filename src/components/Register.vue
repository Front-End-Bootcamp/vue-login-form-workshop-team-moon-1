<script setup>
import NameInput from './Inputs/NameInput.vue';
import MailInput from './Inputs/MailInput.vue';
import PhoneInput from './Inputs/PhoneInput.vue';
import PasswordInput from './Inputs/PasswordInput.vue';
import { ref } from 'vue';

const registerData = ref({
	fullname: "",
	email: "",
	phone: "",
	password: "",
	rePassword: ""
})
</script>

<template>
	<div class="wrapper">
		<pre>{{registerData}}</pre>
		<h1>Register</h1>
		<div>
			<NameInput v-model:name="registerData.fullname"/>
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