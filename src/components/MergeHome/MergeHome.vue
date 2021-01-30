<template>
  <div class="home">
    <div class="home__block">
      <ul class="home__list">
        <li class="home__items"></li>
        <li class="home__items"></li>
        <li class="home__items"></li>
        <li class="home__items"></li>
      </ul>
    </div>
  </div>
</template>

<script>

export default {
  name: 'MergeHome',
}
</script>

<style lang="scss">
  $style: "home";
  .#{$style} {
    &__block {
      background-color: aqua;
      width: 900px;
      height: 600px;
      margin: auto;
    }
    &__list {
      @include flex(space-between, center)
    }
    &__items {
      width: 50px;
      height: 50px;
      background-color: $blue-100;
    }
  }
</style>