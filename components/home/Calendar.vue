<template>
  <div>
    <v-sheet tile height="54" class="d-flex">
      <v-btn icon class="ma-2" @click="$refs.calendar.prev()">
        <v-icon>mdi-chevron-left</v-icon>
      </v-btn>

      <v-spacer></v-spacer>
      <v-btn icon class="ma-2" @click="$refs.calendar.next()">
        <v-icon>mdi-chevron-right</v-icon>
      </v-btn>
    </v-sheet>
    <v-sheet height="600">
      <v-calendar
        ref="calendar"
        v-model="value"
        :weekdays="weekday"
        :type="type"
        :events="events"
        :event-overlap-mode="mode"
        :event-overlap-threshold="30"
        :event-color="getEventColor"
        @change="getEvents"
      ></v-calendar>
    </v-sheet>
  </div>
</template>

<script>
  export default {
    data: () => ({
      type: 'month',
      types: ['month', 'week', 'day', '4day'],
      mode: 'stack',
      modes: ['stack', 'column'],
      weekday: [0, 1, 2, 3, 4, 5, 6],
      weekdays: [
        { text: 'Sun - Sat', value: [0, 1, 2, 3, 4, 5, 6] },
        { text: 'Mon - Sun', value: [1, 2, 3, 4, 5, 6, 0] },
        { text: 'Mon - Fri', value: [1, 2, 3, 4, 5] },
        { text: 'Mon, Wed, Fri', value: [1, 3, 5] },
      ],
      value: '',
      events: [],
      colors: ['red accent-4'],
      names: [],
    }),
    methods: {
      getEvents ({ start, end }) {
        const events = []
        for (let i = 1; i < 32; i++) {
          events.push(
            {
              name: '定休日',
            start: new Date(`2021-08-${i}`),
            color: 'red',
            timed: false,
            }
          )
          i += 6
        }
        for (let i = 5; i < 32; i++) {
          events.push(
            {
              name: '定休日',
            start: new Date(`2021-09-${i}`),
            color: 'red',
            timed: false,
            }
          )
          i += 6
        }
        for (let i = 3; i < 32; i++) {
          events.push(
            {
              name: '定休日',
            start: new Date(`2021-10-${i}`),
            color: 'red',
            timed: false,
            }
          )
          i += 6
        }

        this.events = events
      },
      getEventColor (event) {
        return event.color
      },
      rnd (a, b) {
        return Math.floor((b - a + 1) * Math.random()) + a
      },
    },
  }
</script>

<style>
</style>