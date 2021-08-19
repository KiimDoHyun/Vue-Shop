<template>
  <div>
    <h1>Clicked Item Number is {{ number }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    number: {
      type: Number,
      required: true,
      default: 0,
    },
  },
};
</script>

<style></style>
