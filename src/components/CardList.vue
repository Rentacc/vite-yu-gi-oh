<script>
import CardApp from './CardApp.vue';
import { store } from '../store';

export default {
	data() {
		return {
			store,
		};
	},
	components: {
		CardApp,
	},
};
</script>

<template>
	<div class="bar-black">
		<h2>Found 20 Cards</h2>
	</div>

    <select class="button" name="" id="" placeholder="Seleziona">
        <option value="">Select Filter</option>
    </select>

	<div class="color">
		<div class="cards-container">
			<CardApp
				v-for="(card, index) in store.cardList"
				:key="index"
				class="card-character"
				:card="card"
		/>
		</div>
	</div>
	
</template>

<style lang="scss" scoped>

.bar-black{
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: black;
	margin:1rem 20rem;
	height: 60px;
	h2{
		color: white;
	}
}

.cards-container {
	
	display: flex;
	flex-wrap: wrap;
	.card-character {
	flex: 0 0 25%;
	padding: 3rem;
}
	
}

.button{
	font-size: 20px;
	padding: .6rem;
	margin: 1rem;
}


</style>
