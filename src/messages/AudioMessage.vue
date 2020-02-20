<template>
  <div class="sc-message--text sc-message--audio" :style="messageColors">
    <audio controls="controls">
      <source :src="data.text" type="audio/mpeg">
    </audio>
    <p v-if="data.meta" class='sc-message--meta' :style="{color: messageColors.color}">{{data.meta}}</p>
  </div>
</template>

<script>
  export default {
    props: {
      data: {
        type: Object,
        required: true
      },
      messageColors: {
        type: Object,
        required: true
      },
    }
  }
</script>

<style scoped>
  .sc-message--audio{
    padding: 5px!important;
  }
</style>
