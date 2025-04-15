<script setup>
	import CardReminders from './CardReminders.vue';

	const reminders = [
  { emoji: '💧', title: 'Beber agua', interval: 40 },
  { emoji: '🙆‍♂️', title: 'Estirarse', interval: 20 },
  { emoji: '🧘', title: 'Respirar profundo', interval: 30 },
  { emoji: '🚶‍♀️', title: 'Mover las piernas', interval: 150 }
];
</script>

<template>
	<ul class="reminders">
		<CardReminders
			v-for="reminder in reminders"
			:key="reminder.title"
			:emoji="reminder.emoji"
			:title="reminder.title"
			:default-interval="reminder.interval"
			/>
	</ul>
</template>


