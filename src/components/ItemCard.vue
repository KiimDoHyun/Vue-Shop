<template>
  <div class="cover">
    <div class="item" v-for="n in 10" :key="n">
      <CardComponent :number="n" />
    </div>
  </div>
</template>

<script>
import CardComponent from "./CardComponent.vue";
export default {
  components: {
    CardComponent,
  },
};
</script>

<style>
.cover {
  width: 100%;
  height: 100%;
  background-color: rgb(235, 235, 235);
  padding: 20px;

  /* 상위 컴포넌트에 grid 를 적용하고
  columns 를 1 : 1 : 1 비율로 나눈다.
  */
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(20%, auto));
  /* grid-template-columns: 100px 2fr 1fr; */

  row-gap: 10px;
  column-gap: 10px;
}

.item {
  background-color: white;
  border: 1px solid black;
  border-radius: 5px;
}
</style>
