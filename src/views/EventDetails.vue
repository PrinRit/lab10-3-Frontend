<template>
  <div v-if="event">
    <h1>"Descriptions"</h1>
    <p>{{ event.description }}</p>
    <p>Type</p>
    <p>{{event.type}}</p>
  </div>
</template>

<script>
import EventService from '@/services/EventService.js'
export default {
  props: ['id'],
  data() {
    return {
      event: null
    }
  },
  created() {
    EventService.getEvent(this.id)
      .then((response) => {
        this.event = response.data
      })
      .catch((error) => {
        console.log(error)
      })
  }
}
</script>
