<script setup>
import Toggle from "../components/Toggle.vue";
</script>

<template>
	<header>
		<h1>¿Quieres hacer tilín? ✨🔔</h1>
		<Toggle />
	</header>
</template>

<style>
header {
	width: 100%;
	display: flex;
	align-items: center;
	justify-content: space-around;
	padding: 1rem;
}

h1 {
	font-size: 3rem;
	margin-bottom: 1rem;
	text-align: center;
}
</style>
