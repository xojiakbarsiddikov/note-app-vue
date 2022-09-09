<template>
  <div class="new-note">
    {{/* eslint-disable */}}
    <label>Title</label>
    <input v-model="note.title" type="text">
    <label>Description</label>
    <textarea v-model="note.description"></textarea>
    <button class="btn btnPrimary" @click="addNote">New note</button>
  </div>
</template>

<script>
export default {


  name: "NewNote-v",
  props: {
    note: {
      type: Object
    }
  },
  methods: {
    addNote () {
      console.log(this.note)
      this.$emit('addNote', this.note)
    }
  }
}
</script>

<style lang="scss">
.new-note {
  text-align: center;
}
</style>

