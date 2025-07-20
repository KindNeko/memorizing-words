<script setup>
import Button from './components/Button.vue';
import Card from './components/Card.vue';
import Header from './components/Header.vue';

const data = {
	number: '01',
	title: 'unadmitted',
	action: 'Перевернуть',
};

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
		<Card v-bind="data" @flip="flip" @answer="answer" />
		<Button> Начать игру </Button>
	</main>
</template>

<style scoped></style>
