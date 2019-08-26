<template>
  <span class="heightComponent">
    身長:{{height}}
    <button @click="clickHandler(1)">+</button>
    <button @click="clickHandler(-1)">+</button>
  </span>
</template>

<script>
export default {
  props: {
    height: Number,
    changeHeight: Function,
    id: Number
  },
  methods: {
    clickHandler(value) {
      this.changeHeight(this.id, value);
    }
  }
};
</script>

<style scoped>
.heightComponent {
  border: 1px solid green;
}
</style>

