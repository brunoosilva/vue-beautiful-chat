<template>
  <audio controls="controls">
    <source :src="data.text" type="audio/mpeg">
  </audio>
</template>

<script>
  export default {
    props: {
      data: {
        type: Object,
        required: true
      }
    }
  }
</script>
