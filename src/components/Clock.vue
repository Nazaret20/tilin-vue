<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const currentTime = ref(new Date());

// Función para actualizar el tiempo
const updateTime = () => {
	currentTime.value = new Date();
};

let timerInterval;

// Iniciar el temporizador al montar el componente
onMounted(() => {
	// Actualizar inmediatamente y luego cada segundo
	updateTime();
	timerInterval = setInterval(updateTime, 1000);
});

// Limpiar el temporizador cuando el componente se desmonte
onUnmounted(() => {
	clearInterval(timerInterval);
});

// Formato de hora personalizado
const formattedTime = () => {
	const hours = currentTime.value.getHours().toString().padStart(2, "0");
	const minutes = currentTime.value.getMinutes().toString().padStart(2, "0");
	const seconds = currentTime.value.getSeconds().toString().padStart(2, "0");
	return `${hours}:${minutes}:${seconds}`;
};
</script>

<template>
	<p class="clock">{{ formattedTime() }}</p>
</template>

<style scoped>
.clock {
    font-size: 4rem;
}
</style>
