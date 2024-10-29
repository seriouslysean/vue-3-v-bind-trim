<template>
  <h1>v-mode.trim</h1>
  <fieldset>
    <label>Standard Input</label>
    <hr />
    <input v-model.trim="inputValue" />
    <hr />
    <code>Current Value: "{{ inputValue }}"</code>
  </fieldset>
  <hr />
  <fieldset>
    <label>Custom Input</label>
    <hr />
    <BaseInput v-model.trim="inputValue" />
    <hr />
    <code>Current Value: "{{ inputValue }}"</code>
  </fieldset>
</template>

<script>
import BaseInput from './components/BaseInput.vue';

export default {
  name: 'App',
  components: {
    BaseInput,
  },
  data() {
    return {
      inputValue: '',
    };
  },
};
</script>

<style scoped></style>
