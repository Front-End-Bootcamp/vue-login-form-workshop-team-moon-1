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
	<div class="register__wrapper">
		<pre>{{registerData}}</pre>
		<h1 class="register__header">Register</h1>
		<div class="register__inputWrapper">
			<NameInput v-model:name="registerData.fullname" />
			<MailInput />
			<PhoneInput />
			<PasswordInput />
			<PasswordInput />
		</div>
		<div class="register__Buttons">
			<button class="register__regBtn">Register</button>
			<button class="register__loginBtn">Have an account</button>
		</div>
	</div>
</template>

<style lang="scss" scoped>
.register {
	&__wrapper {
		width: 500px;
		border-radius: 10px;
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		background-color: wheat;

		background: rgba(255, 255, 255, 0.25);
		box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
		backdrop-filter: blur(4px);
		-webkit-backdrop-filter: blur(4px);
		border-radius: 10px;
		border: 1px solid rgba(255, 255, 255, 0.18);
	}

	&__inputWrapper {
		display: flex;
		width: 80%;
		border: solid;
		border-radius: 10px;
		margin-bottom: 10px;
		border-color: rgb(81, 81, 246);

		input {
			display: flex;
			outline: none;
			border: none;
			color: black;
			font-size: 24px;
			height: 35px;
			background-color: #252cff00; // transparent
			width: 100%;
		}

	}

	&__header {
		color: #252EFF;
	}

	&__Buttons {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
	}

	&__regBtn {
		display: flex;
		justify-content: center;
		align-items: center;
		background-color: rgb(139, 84, 255);
		color: white;
		width: 400px;
		margin-top: 10px;
		border-radius: 50px;

	}

	&__regBtn:hover {
		background-color: rgb(118, 56, 253);
	}

	&__loginBtn {
		display: flex;
		justify-content: center;
		align-items: center;
		background: rgb(96, 102, 255);
		color: white;
		width: 400px;
		margin-top: 10px;
		border-radius: 50px;
		margin-bottom: 15px;
	}

	&__loginBtn:hover {
		background-color: rgb(11, 18, 243);
	}


	&__wrapper-dark {
		display: flex;
		flex-direction: column;
		background-color: black;

		&__header-dark {
			color: white;
		}
	}
}
</style>