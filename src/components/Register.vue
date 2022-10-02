<script setup>
import NameInput from './Inputs/NameInput.vue';
import MailInput from './Inputs/MailInput.vue';
import PhoneInput from './Inputs/PhoneInput.vue';
import PasswordInput from './Inputs/PasswordInput.vue';

</script>

<template>
	<div>
		<h1>Register</h1>
		<div>
			<NameInput />
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