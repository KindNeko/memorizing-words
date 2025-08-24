<script setup>
import { ref } from 'vue';
import Button from './components/Button.vue';
import Card from './components/Card.vue';
import Header from './components/Header.vue';

const number = ref('01');
const word = ref('unadmitted');
const state = ref('Перевернуть');

const translation = ref('непризнаный');
const status = ref(true);

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
			:state="state"
			@flip="flip"
			@answer="answer"
		/>
		<Card
			:number="number"
			:status="status"
			:translation="translation"
			:state="state"
			@flip="flip"
			@answer="answer"
		/>
		<Button> Начать игру </Button>
	</main>
</template>

<style scoped></style>
