<script setup>
import { ref } from 'vue';
import Score from './Score.vue';
let score = ref('100');
</script>

<template>
	<header class="header">
		<section class="header__section">
			<h3 class="header__title">Запомните слово</h3>
			<Score :score="score" />
		</section>
	</header>
</template>

<style scoped>
.header {
	color: var(--color-secondary);
	font-weight: 700;
	font-size: 16px;
	line-height: 24px;
	display: flex;
	justify-content: space-between;
	align-items: center;
	width: 100%;
}
.header__section {
	width: 100%;
	display: flex;
	justify-content: space-between;
	padding: 37px 62px 0 66px;
}
</style>
