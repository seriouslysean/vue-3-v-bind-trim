<template>
  <input ref="input" class="base-input" :foo="modelValue" @input="onInput" />
</template>

<script>
export default {
  name: 'BaseInput',
  props: {
    modelValue: {
      type: String,
      default: '',
    },
  },
  methods: {
    onInput(e) {
      this.$emit('update:modelValue', e.target.value);
    },
  },
};
</script>

<style scoped></style>
