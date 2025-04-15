<script setup>
import HeaderComp from "./components/HeaderComp.vue";
import Reminders from "./components/Reminders.vue";
import Clock from "./components/Clock.vue";
</script>

<template>
	<HeaderComp />
	<main class="main">
		<section class="section">
			<Reminders />
		</section>
		<aside class="aside">
			<div>
				<p class="done">¡Muy bien! Continúa así...</p>
				<p class="motivation">¡Eres increíble!</p>
			</div>
			<Clock/>
		</aside>
	</main>
</template>

<style scoped>
.main {
	width: 100%;
	height: 100%;
	padding-top: 1rem;
	display: flex;
	gap: 2rem;
	justify-content: center;
}
.section {
	width: 50%;
	height: 100%;
}
.aside {
	width: 40%;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	gap: 4rem;
}

.done {
    margin-bottom: 1rem;
}
</style>
