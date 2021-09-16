<template>
  <h1>"Descriptions"</h1>
  <p>{{ event.description }}</p>
  <p>{{ event.type }}</p>
</template>

<script>
export default {
  props: ['event']
}
</script>
