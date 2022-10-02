<script setup>
import Register from './components/Register.vue';
import Login from './components/Login.vue';
import { ref } from 'vue';
	const isLogin = ref(false)
</script>

<template>
	<Register/>
	<Login v-if="isLogin"/>
</template>

<style scoped>

</style>
