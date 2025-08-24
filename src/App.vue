<script setup>
import { ref } from 'vue';
import Button from './components/Button.vue';
import Card from './components/Card.vue';
import Header from './components/Header.vue';

const number = ref('01');
const word = ref('unadmitted');
const action = ref('Перевернуть');

const translations = ref('непризнаный');
const state = ref(false);
const opened = ref(false);

function flip(flip) {
	console.log(flip);
}
function answer(answer) {
	console.log(answer);
}
</script>

<template>
	<Header />
	<main class="main">
		<Card
			:number="number"
			:word="word"
			:action="action"
			@flip="flip"
			@answer="answer"
		/>
		<Button> Начать игру </Button>
	</main>
</template>

<style scoped></style>
