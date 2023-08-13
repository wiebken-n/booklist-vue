<template>
  <button :class="cssClass" @click="$emit('btn-clicked')">
    <slot />
  </button>
</template>
<script>
export default {
  methods: {
    emit() {
      this.$emit("btn-clicked");
    },
  },
  computed: {
    cssClass() {
      return `btn btn--${this.variant}`;
    },
  },
  name: "BaseButton",
  props: {
    // text: {
    //   type: String,
    //   default: "Click me",
    // },
    variant: {
      type: String,
      default: "secondary",
    },
  },
};
</script>

<style scoped>
.btn {
  border: 3px solid transparent;
  border-radius: 3px;
  padding: 5px;
  cursor: pointer;
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 0.125rem;
  align-items: center;
}

.btn--primary {
  border-color: var(--primary-dark);
  background-color: var(--primary);
  color: #fff;
}

.btn--primary:hover {
  border-color: var(--primary);
  background-color: var(--primary-dark);
}

.btn--secondary {
  border-color: var(--primary);
  background-color: transparent;
  color: var(--primary);
}

.btn--secondary:hover {
  background-color: var(--primary);
  color: #fff;
}
</style>
