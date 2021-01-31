<template>
  <component :is="getIcon"></component>
</template>

<script>

const getName = (name) => `icon-${name}`;

export default {
  name: 'Icon',
  props: {
    icon: {
      type: String,
      default: 'merge-logo'
    },
  },
  components: {
    [getName('merge-logo')]: () => import('../Icons/MergeLogo'),
  },
  computed: {
    getIcon() {
      return getName(this.icon);
    },
  },
}
</script>