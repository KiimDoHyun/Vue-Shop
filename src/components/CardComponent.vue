<template>
  <!-- 자식 -->
  <router-link
    :to="{ name: 'Detail', params: { number: number } }"
    class="link"
  >
    <div class="contentsCover">
      <div class="imageSection"></div>
      <div class="textSection">
        <h3>Item Number : {{ number }}</h3>
      </div>
    </div>
  </router-link>
</template>

<script>
export default {
  data() {
    return {
      // 이러면 중복이라고 에러뜸.
      //   number: 100000,
    };
  },
  props: {
    number: {
      type: Number,
      required: true,
      default: 0,
    },
  },
};
</script>

<style>
.contentsCover {
  width: 100%;
  height: 100%;
}
.imageSection {
  width: 100%;
  height: 60%;
  background-color: rgba(199, 199, 199, 0.479);
}
.textSection {
  width: 100%;
  height: auto;
  padding: 5px;
  color: black;
}

.link {
  text-decoration: none;
}
</style>
