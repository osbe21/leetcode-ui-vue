<script setup>
import CardContainer from './components/CardContainer.vue';
import Card from './components/Card.vue'

</script>

<template>
<CardContainer direction="row">

	<template #1>
		<Card></Card>
	</template>

	<template #2>

		<CardContainer direction="column">
			
			<template #1>
				<Card></Card>
			</template>
			
			<template #2>
				<Card></Card>
			</template>
	
		</CardContainer>
	</template>
	
</CardContainer>
</template>

<style scoped>

</style>
