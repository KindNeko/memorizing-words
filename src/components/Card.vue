<script setup>
const props = defineProps({
	number: String,
	title: String,
	action: String,
});

const emits = defineEmits({
	flip: null,
	answer: null,
});

function flipCard() {
	emits('flip', 'Перевернуто');
}

function answerCard() {
	emits('answer', 'Правильно');
}
</script>

<template>
	<div class="card">
		<div class="card__wrapper" @click="answerCard">
			<p class="card__number">{{ number }}</p>
			<p>{{ title }}</p>
			<p class="card__action" @click="flipCard">{{ action }}</p>
		</div>
	</div>
</template>

<style scoped>
.card {
	width: 250px;
	height: 378px;
	box-shadow: 0px 0px 16px 0px #0000001a;
	border-radius: 16px;
	padding: 28px 19px;
	background: #ffffff;
	color: #000000;
	position: relative;
}

.card__wrapper {
	border: 1px solid #cce8ff;
	border-radius: 12px;
	width: 100%;
	height: 100%;
	text-align: center;
	display: flex;
	align-items: center;
	justify-content: center;
}

.card__number {
	position: absolute;
	top: 20px;
	left: 35px;
	background: #fff;
	font-size: 14px;
}

.card__action {
	font-weight: 700;
	font-size: 12px;
	color: var(--color-secondary);

	position: absolute;
	bottom: 19px;
	left: 84px;
	right: 77px;
	background: #fff;
	text-transform: uppercase;
}
</style>
