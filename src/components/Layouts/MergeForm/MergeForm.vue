<template>
  <div class="form">
    <div class="form__wrapper">
      <a href="/" class="form__logo">
        <m-icon name=merge-logo />
      </a>
      <form action="/login" method="post" class="form__form">
        <h3 class="form__heading">Sign in</h3>
        <p class="form__description">
          Don't have an account?
          <a href="/sign-up" class="form__sign-up">Sign up now</a>
        </p>
        <div class="form__inputs">
          <label for="email" class="form__label">Email</label>
          <input type="email" name="email" id="email" class="form__input">

          <label for="password" class="form__label">Password</label>
          <input type="password" name="password" id="password" class="form__input">
        </div>
        <button type="submit" class="form__submit-btn">Sign in</button>
      </form>
    </div>
    <ul class="form__nav-list">
      <li class="form__items">
        <a href="/" class="form__item-link">Conact</a>
      </li>
      <li class="form__items">
        <a href="/" class="form__item-link">Privacy</a>
      </li>
      <li class="form__items">
        <a href="/" class="form__item-link">Terms</a>
      </li>
    </ul>
  </div>
</template>

<script>
import MIcon from '@/components/common/MIcon.vue';

export default {
  name: 'MergeForm',
  components: {
    MIcon,
  }
}
</script>

<style lang="scss">
  $style: "form";
  .#{$style} {
    @include flex(space-between, stretch, column);
    flex-basis: 420px;
    max-width: 420px;
    &__logo {
      display: block;
      margin-bottom: 112px;
    }
    &__heading {
      @include text($H280, 700, $grey-100);
      line-height: 34px;
      margin-bottom: 15px;
    }
    &__description {
      @include text($H40, 600, $grey-100);
      line-height: 24px;
      margin-bottom: 61px;
    }
    &__sign-up {
      @include text($H40, 600, $blue-100);
      margin-left: 9px;
      transition: color .3s ease-in;
      &:hover,
      &:active {
        color: $blue-80;
      }
      &:visited {
        color: $grey-30;
      }
    }
    &__inputs {
      @include flex(center, stretch, column);
    }
    &__label {
      @include text($H40, 600, $grey-100);
      line-height: 24px;
      margin-bottom: 14px;
    }
    &__input {
      @include text($H40, 600, $grey-100);
      display: block;
      line-height: 17px;
      padding: 18px 20px 18px 20px;
      width: 100%;
      margin-bottom: 30px;
      border: 1px solid $white-10;
      border-radius: 8px;
      outline: none;
      &:focus,
      &:active {
        border-color: $blue-100;
      }
    }
    &__submit-btn {
      flex-basis: 420px;
      max-width: 420px;
      width: 100%;
      height: 57px;
      border: none;
      border-radius: 8px;
      background-color: $blue-100;
      @include text($H200, 600, $white-100);
      font-family: $main-text;
      line-height: 20px;
      position: relative;
      cursor: pointer;
      transition: background-color .3s ease-in;
      &:after {
        content: "";
        position: absolute;
        bottom: 0;
        display: block;
        width: 90%;
        height: 22px;
        background-color: $blue-100;
        filter: blur(16px);
        border-radius: 8px;
        left: 50%;
        transform: translateX(-50%);
        z-index: -1;
        transition: background-color .3s ease-in;
        transition: filter .3s ease-in;
      }
      &:hover {
        background-color: $blue-70;
        &:after {
          filter: blur(22px);
          background-color: $blue-70;
        }
      }
      &:active {
        background-color: $blue-100;
        &:after {
          background-color: rgba($blue-100, .5);
        }
      }
      &:disabled {
        background-color: $blue-10;
        cursor: not-allowed;
        &:after {
          background-color: transparent;
        }
      }
      &:focus {
        outline: none;
      }
    }
    &__nav-list {
      @include flex(flex-start, center);
      flex-basis: 204px;
      max-height: 24px;
    }
    &__items {
      margin-right: 25px;
      &:last-child {
        margin-right: 0px;
      }
    }
    &__item-link {
      @include text($H40, 600, $grey-30);
      line-height: 24px;
      display: inline-block;
      transition: color .3s ease-in;
      &:hover,
      &:active {
        color: $grey-100;
      }
    }
  }
</style>