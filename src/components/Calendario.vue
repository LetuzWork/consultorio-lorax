<template>
    <div class="calendario">
      <FullCalendar :options="calendarOptions" />
      <button @click="toggleWeekends">toggle weekends</button>
    </div>
</template>

<script>
/* eslint-disable */
import '@fullcalendar/core/vdom' // solves problem with Vite
import FullCalendar from '@fullcalendar/vue3'
import dayGridPlugin from '@fullcalendar/daygrid'
import interactionPlugin from '@fullcalendar/interaction'

export default {
  name: 'Calendario',
  data () {
		return { 
      calendarOptions: {
        plugins: [ dayGridPlugin, interactionPlugin ],
        initialView: 'dayGridMonth',
        dateClick: this.handleDateClick,
        events: [
          { title: 'event 1', date: '2022-01-01' },
          { title: 'event 2', date: '2022-01-02' }
        ],
        weekends: false
      }
    }
	},
	components: {
		FullCalendar
	},
	methods: {
		handleDateClick: function(arg) {
      alert('date click! ' + arg.dateStr)
    },
    toggleWeekends: function() {
      this.calendarOptions.weekends = !this.calendarOptions.weekends // toggle the boolean!
    }
	}
}
</script>

<style lang="scss" scoped>


</style>