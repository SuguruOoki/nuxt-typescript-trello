<template>
  <v-card color="teal lighten-5">
    <v-card-actions>
      <v-text-field v-model="title" label="Add a list..." @keyup.enter="addList()"/>
    </v-card-actions>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

export default Vue.extend({
  data() {
    return {
      title: ''
    }
  },
  methods: {
    addList() {
      this.$store.dispatch('lists/add', this.title)
      this.title = ''
    }
  }
})
</script>
