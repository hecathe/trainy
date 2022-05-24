<template>
	<div class="container">
		<h1>Events</h1>
		<event-list :events="events"/>
	</div>
</template>

<script>
import EventList from '@/components/EventList.vue';
import axios from 'axios';

export default {
	components: {
		EventList
	},
	name: 'EventsPage',
	data() {
		return {
			events: []
		}
	},
	methods: {
		async fetchEvents() {
			try {
				const response = await axios.get('https://jsonplaceholder.typicode.com/users');
				// console.log(response);
				this.events = response.data
			} catch (error) {
				console.log(error);
			}
		}
	},
	mounted() {
		this.fetchEvents()
	}
}
</script>

<style>
	body {
		font-family: 'Courier New', Courier, monospace;
		margin: 0;
		padding: 20px;
		padding-bottom: 60px;
	}

	.container {
		max-width: 1440px;
		margin: 0 auto;
	}
</style>