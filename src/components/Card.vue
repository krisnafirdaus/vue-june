<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})

const data = [
  {
    id: 1,
    title: "Card 1",
    content: "This is card 1",
  },
  {
    id: 2,
    title: "Card 2",
    content: "This is card 2",
  },
  {
    id: 3,
    title: "Card 3",
    content: "This is card 3",
  },
];
</script>

<template>
  <div>
    <h1>{{ msg }}</h1>
		<div v-for="item in data" :key="item.id">
			<h2>{{ item.title }}</h2>
			<p>{{ item.content }}</p>
		</div>
  </div>
</template>

<style scoped>
h1 {
  color: red;
}
</style>
