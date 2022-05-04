<template>
  <div class="text-center">
    <img src="../../assets/park.png" />
    <hr />
    <h1 v-text="title"></h1>
    <hr />
  </div>
</template>

<script>
export default {
  props: ["title"],
};
</script>


<style scoped>
img {
  max-width: 150px;
}
</style>