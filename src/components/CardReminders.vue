<script setup>
defineProps({
  emoji: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  defaultInterval: {
    type: Number,
    default: 30
  }
});
</script>

<template>
	<li class="reminder-card">
		<h2 class="reminder-title">{{ emoji }} {{ title }}</h2>
		<div class="reminder-settings">
			<span class="interval-label">Recordarme cada:</span>
			<input type="number" :value="defaultInterval" min="1" class="interval-input" />
			<span class="interval-unit">minutos</span>
		</div>
	</li>
</template>

<style scoped>
 .reminder-card {
      background-color: var(--bg-card);
      border-radius: 1.2rem;
      margin-bottom: 1.6rem;
      padding: 1.6rem;
      box-shadow: 0 2px 8px var(--shadow);
      display: flex;
      flex-direction: column;
    }

    .reminder-title {
      font-size: 1.8rem;
      font-weight: 500;
      margin: 0 0 12px 0;
      color: var(--text);
    }

    .reminder-settings {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .interval-label {
      color: var(--secondary-text);
    }

    .interval-input {
      background-color: var(--bg-input);
      border: 1px solid var(--border);
      border-radius: 8px;
      color: var(--text);
      padding: .6rem 1.2rem;
      width: 7rem;
      text-align: center;
      margin-left: .8rem;
    }

    .interval-input:focus {
      outline: none;
      box-shadow: 0 0 0 2px rgba(207, 245, 255, 0.3);
    }

    .interval-unit {
      color: var(--secondary-text);
      margin-left: .8rem
    }

    input[type="number"]::-webkit-outer-spin-button,
    input[type="number"]::-webkit-inner-spin-button {
      -webkit-appearance: none;
      margin: 0;
    }
    </style>
