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

  beforeCreate() {
    console.log("beforeCreate");
  },

  created() {
    console.log("Created");
  },

  beforeMount() {
    console.log(2);
  },

  mounted() {
    console.log(3);
  },
};
</script>

<style></style>
