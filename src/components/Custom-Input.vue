<template>
  <label
    >{{ label }}
    <input type="text" v-model="inputValue" :placeholder="placeholder" />
  </label>
</template>

<script>
export default {
  props: ["label", "placeholder", "modelValue"],
  name: "CustomInput",
  computed: {
    inputValue: {
      get() {
        return this.modelValue;
      },
      set(value) {
        this.$emit("update:modelValue", value);
      },
    },
  },
  methods: {
    // val() {
    //   console.log(this.modelValue);
    // },
  },
};
</script>
<style></style>
