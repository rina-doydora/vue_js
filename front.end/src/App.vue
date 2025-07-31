<script lang="ts" setup>
import { ref } from 'vue';


const message = ref('Task');
const newTask = ref("");

function formSubmitted() {
    console.log(newTask.value);
}
</script>

<template>
 <main>
   <hi>{{  message }}</hi>
 <form>
     <label>
        New task
        <input v-model="newTask" name="newTask" />
      </label>
      <div class="button-container">
        <button>Add</button>
        <h3>{{  newTask }}</h3>
      </div>
    </form>

  </main>
</template>


<style scope>
main {
  max-width: 800px;
  margin: 1rem auto;
}

.button-container {
   display: flex;
   justify-content: end;
  }
  </style>

