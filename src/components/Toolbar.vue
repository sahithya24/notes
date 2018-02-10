<template>
  <div id="toolbar">
    <i @click="addNote" uk-icon="icon: plus"></i>
    <i @click="toggleFavorite"
      uk-icon="icon: star"
      :class="{starred: activeNote.favorite}"></i>
    <i @click="deleteNote" uk-icon="icon: minus"></i>
  </div>
</template>

<script>
import { addNote, deleteNote, toggleFavorite } from '../vuex/actions'
export default {
  vuex: {
    getters: {
      activeNote: state => state.activeNote
    },
    actions: {
      addNote,
      deleteNote,
      toggleFavorite
    }
  }
}
</script>
