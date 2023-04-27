<script>
export default {
  name: 'Main',

}
</script>

<template>
  <div>
    <h1>Da fare domani =></h1>
  </div>
</template>

<style lang="scss" scoped>
  @import '../scss/partials/variables';

  div{
    height: 200px;
    background-color: black;
    padding: 20px;
    @include flexMe(vertical)
  }
</style>