<template>
  <router-link
    :class="{ 'tw-font-bold tw-border-primary': isCurrentRoute }"
    :to="{ name: to, params: toParams }"
    class="route tw-p-4 tw-block tw-border-t-4 tw-border-transparent"
    exact
  >
    <slot></slot>
  </router-link>
</template>

<script>
export default {
  name: "bar",

  props: {
    to: {
      type: String,
      required: false
    },

    toParams: {
      type: Object,
      default: () => {
        return {};
      }
    }
  },

  computed: {
    isCurrentRoute() {
      return this.$route.name === this.to;
    }
  }
};
</script>
