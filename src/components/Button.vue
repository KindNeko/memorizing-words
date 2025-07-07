<script setup></script>

<template>
	<button class="button">
		<slot />
	</button>
</template>

<style scoped>
.button {
	border: none;
	border-radius: 50px;
	width: 315px;
	background: var(--color-bg-btn);
	padding: 16px 10px;
	font-family: var(--font);
	font-size: 24px;
	font-weight: 400;
	color: var(--primary);
	cursor: pointer;
}
</style>
