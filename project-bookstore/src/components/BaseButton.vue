<template>
  <button :class="styling">{{ text }}</button>
  <!-- <button :class="['base-button', variantClass]">{{ text }}</button> -->
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: true,
    },
    variant: {
      type: String,
      default: "primary",
      validator(value) {
        return ["primary", "secondary"].includes(value);
      },
      //   validator: (value) => ["primary", "secondary"].includes(value),
    },
  },

  computed: {
    styling() {
      return ["btn", `btn--${this.variant}`];
    },
    // variantClass() {
    //   return this.variant === "secondary" ? "bg--secondary" : "bg--primary";
    // },
  },
};
</script>

<style scoped>
.base-button {
  padding: 5px 10px;
  border: none;
  border-radius: 5px;
  color: #fff;
  cursor: pointer;
}

.bg--primary {
  background-color: var(--primary);
}

.bg--secondary {
  background-color: var(--secondary);
}
</style>
