<script setup>
import { ref } from 'vue';
import Button from './components/Button.vue';
import Card from './components/Card.vue';
import Header from './components/Header.vue';

const score = ref('100');
const cards = ref([
	{
		number: '01',
		word: 'unadmitted',
		translation: 'непризнанный',
		state: 'Перевернуть',
		status: true,
	},
]);

function flip(flip) {
	console.log(flip);
}
function answer(answer) {
	console.log(answer);
}
</script>

<template>
	<Header :score="score" />
	<main class="main">
		<Card
			v-for="card in cards"
			:key="card.number"
			:number="card.number"
			:word="card.word"
			:translation="card.translation"
			:state="card.state"
			:status="card.status"
			@flip="flip"
			@answer="answer"
		/>
		<Button> Начать игру </Button>
	</main>
</template>

<style scoped></style>
