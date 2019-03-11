<template>
  <div id="app">
    <div id="calendar-week" class="container">
		<!-- Markup for the calender week -->
		<CalendarDay v-for="day in sharedState.seedData" :key="day.id" :day="day" />
    </div>
  </div>
</template>

<script>
import { store } from '../store.js';
import CalendarDay from './CalendarDay.vue';
export default {
	name: 'CalendarWeek',
	data () {
		return {
			sharedState: store.state
		}
	},
	components: {
		CalendarDay
	}
}
</script>


<style lang="scss" scoped>
#calendar-week {
  margin-bottom: 50px;
  .column {
    padding: 0 0 0 0;
  }
}
</style>