<template>
	<div>
		<h1>Events</h1>
		<event-list :events="events"/>
	</div>
</template>

<script>
import EventList from '@/components/EventList.vue'

export default {
	components: {
		EventList
	},
	name: 'EventsPage',
	data() {
		return {
			events: ['1', '2']
		}
	}
}
</script>

<style>
	body {
		font-family: 'Courier New', Courier, monospace;
	}
</style>