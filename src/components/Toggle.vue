<script setup></script>

<template>
	<div class="theme-toggle">
		<input type="checkbox" id="toggle-theme" />
		<label for="toggle-theme">
			<span class="moonSun"></span>
		</label>
	</div>
</template>

<style scope>
.theme-toggle {
	position: relative;
	width: 6rem;
	height: 3rem;
}

.theme-toggle input {
	display: none;
}

.theme-toggle label {
	display: block;
	width: 100%;
	height: 100%;
	background-color: var(--bg-input);
	border-radius: 5rem;
	position: relative;
	cursor: pointer;
	transition: background-color 0.3s ease;
	padding: 0.4rem;
	box-sizing: border-box;
}

.theme-toggle .moonSun {
	width: 2.1rem;
	height: 2.1rem;
	background-color: var(--moonSun);
	border-radius: 50%;
	position: absolute;
	top: 0.5rem;
	left: 0.5rem;
	transition: all 0.4s ease;
}

.theme-toggle .moonSun::before {
	content: "";
	position: absolute;
	width: 1.6rem;
	height: 1.6rem;
	top: 0.1rem;
	right: -0.1rem;
	background: var(--bg-input);
	border-radius: 50%;
	transition: opacity 0.3s ease;
}

.theme-toggle input:checked + label {
	background-color: var(--bg-input);
}

.theme-toggle input:checked + label .moonSun {
	left: 3.4rem;
	background-color: var(--moonSun);
}

.theme-toggle input:checked + label .moonSun::before {
	opacity: 0;
}
</style>
