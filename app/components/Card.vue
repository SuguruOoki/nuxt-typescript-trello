<template>
  <v-card>
    <v-card-text>{{ card.body }}</v-card-text>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

export default Vue.extend({
  props: {
    card: {
      type: Object,
      required: true
    }
  }
})
</script>
