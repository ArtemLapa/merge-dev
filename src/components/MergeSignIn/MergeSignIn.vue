<template>
  <div class="sign-in">
    <merge-carousel class="sign-in__carousel-wrapper" />
    <merge-form />
  </div>
</template>

<script>
import MergeCarousel from '@/components/Layouts/MergeCarousel/MergeCarousel.vue';
import MergeForm from '@/components/Layouts/MergeForm/MergeForm.vue';

export default {
  name: 'MergeSignIn',
  components: {
    MergeCarousel,
    MergeForm,
  },
}
</script>

<style lang="scss">
  $style: "sign-in";
  .#{$style} {
    @include flex(center, stretch);
    &__carousel-wrapper {
      background-color: $blue-100;
      height: 860px;
      width: 800px;
      margin-right: 80px;
      border-radius: 15px;
    }
  }
</style>