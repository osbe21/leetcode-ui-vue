<script setup>
import Navbar from './components/Navbar.vue';
import CardContainer from './components/CardContainer.vue';
import Card from './components/Card.vue'
import DescriptionCard from './components/DescriptionCard.vue';
import CodeCard from './components/CodeCard.vue';

</script>

<template>
<div id="page">
	<Navbar />

	<CardContainer direction="row">

		<template #1>
			<DescriptionCard />
		</template>

		<template #2>

			<CardContainer direction="column">
				
				<template #1>
					<CodeCard />
				</template>
				
				<template #2>
					<Card>
						<template #icon>
							<i class="fa-regular fa-square-check" style="color: #3ba027;"></i>
						</template>
						<template #title>
							<span>Testcase</span>
						</template>
					</Card>
				</template>
		
			</CardContainer>
		</template>
		
	</CardContainer>
</div>
</template>

<style scoped>
#page {
	width: 100%;
	height: 100%;

	padding: 5px 10px;

	display: flex;
	flex-direction: column;
	align-items: stretch;
	gap: 5px;
}
</style>
