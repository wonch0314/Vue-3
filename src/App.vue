<template>
  <div class='container'>
    <h1>To Do List</h1>
    <form action="">
      <input
        type="text"
        v-model='name'
        @input='updateName'
      >
      <button
        class='btn btn-primary'
        @click='onSubmit'
      >
        Click
      </button>
    </form>
  </div>

</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const name = ref('Chanho Won')
    const onSubmit = () => {
      alert(name.value)
    }
    const updateName = (e) => {
      name.value = e.target.value
    }


  return {
    name,
    onSubmit,
    updateName,
  }

  }
}
</script>

<style>
  .name {
    color: red;
  }
</style>