<script setup>
import Heath from './icons/Heath.vue';
const num = defineProps({
	score: String,
});
</script>

<template>
	<div class="score">
		<div>{{ score }}</div>
		<Heath />
	</div>
</template>

<style scoped>
.score {
	display: flex;
	background: #cce8ff;
	padding: 12px 24px;
	max-width: 110px;
	justify-content: center;
	border-radius: 36px;
	gap: 10px;
	color: #008bfe;
}
</style>
