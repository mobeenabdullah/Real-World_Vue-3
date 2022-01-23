<template>
  <h1>Events for Good</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "Home",
  components: {
    EventCard
  },
  data() {
    return {
      events: [
        {
          id: 3432231,
          category: 'animal welfare',
          title: 'Cat Adoption Day',
          description: 'Find your new feline friend at this event',
          location: 'Meow Town',
          date: 'January 28, 2022',
          time: '12:00',
          petsAllowed: true,
          organizer: 'Kat Laydee'
        },
        {
          id: 433443,
          category: 'animal welfare',
          title: 'Cat Adoption Day 2',
          description: 'Find your new feline friend at this event',
          location: 'Meow Town',
          date: 'February 28, 2022',
          time: '09:00',
          petsAllowed: true,
          organizer: 'Jill Laydee'
        },
        {
          id: 566433,
          category: 'animal welfare',
          title: 'Cat Adoption Day 3',
          description: 'Find your new feline friend at this event',
          location: 'Meow Town',
          date: 'March 28, 2022',
          time: '06:00',
          petsAllowed: true,
          organizer: 'John Laydee'
        }
      ]
    }
  }
}
</script>

<style scoped>
  .events {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>