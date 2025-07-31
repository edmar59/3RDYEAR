<script lang="ts" setup>
import { ref } from 'vue'

const message = ref('Task')
const newSecurity = ref("")

function formSubmitted() {
  console.log(newSecurity.value)
}
</script>

<template>
  <main>
    <h1>{{ message }}</h1>
    <form @submit.prevent="formSubmitted">
      <label>
        New task
        <input v-model="newSecurity" name="newTask" />
      </label>
      <div class="button-container">
        <button>Add</button>
      </div>
    </form>
  </main>
</template>

<style scoped>
main {
  max-width: 800px;
  margin: 1rem auto;
}

.button-container {
  display: flex;
  justify-content: flex-end;
}
</style>
