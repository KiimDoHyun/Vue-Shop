<template>
  <v-container>
    <v-row class="row mb-5">
      <v-col class="col mr-3" cols="5"></v-col>
      <v-col class="col" cols="4"></v-col>
    </v-row>
    <v-row class="row mb-5">
      <v-col class="col mr-3" cols="5"></v-col>
      <v-col class="col" cols="4"></v-col>
      <div>
        <h1>Clicked Item Number is {{ number }}</h1>
      </div>
    </v-row>
  </v-container>
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

<style>
.row {
  background-color: red;
}

.col {
  background-color: blue;
}
</style>
