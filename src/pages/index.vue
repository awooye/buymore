<template>
  <div class="index">
    <div class="container">
      <div class="box">index</div>
    </div>
  </div>
</template>
<script>
export default {
  name: "index",
};
</script>
<style lang="scss">
@import "./../assets/scss/base.scss";
.index {
  .container {
    .box {
      position: absolute;
      width: 200px;
      background-color: #f00;
    }
  }
}
</style>