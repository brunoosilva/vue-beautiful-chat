<template>
  <div class="sc-message--text" :style="messageColors">
    <div
      :style="{
        backgroundImage: 'url(' + data.image + ')',
        width: '100%',
        height: '100px',
        'background-size': 'cover',
        margin: '10px 0',
      }"
    ></div>
    <p class="sc-message--text-content">{{data.text}}</p>
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
