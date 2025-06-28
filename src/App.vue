<script setup>
const currentDate = new Date();

const day = currentDate.getDate();
const month = currentDate.getMonth() + 1;
const year = currentDate.getFullYear();

const dateString = `${day}.${month}.${year}`;
</script>

<template>
	<div>{{ dateString }}</div>
</template>

<style scoped></style>
